# star_rsem

STAR-RSEM pipeline of Lee et al., 2020 for bulk RNA-seq data 

## Set-up

- Install `conda` and `bioconda` (for GNU/Linux)

```console
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
sh Miniconda3-latest-Linux-x86_64.sh
```

- Set-up conda channels

```console
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
```

- Create a dedicated `conda` environment (optional)

```console
conda create --name star_rsem
```

- Activate environment

```console
conda activate star_rsem
```

- Install softwares/pacakges

```console
conda install fastqc
conda install multiqc
conda install trimmomatic
conda install star=2.5.3a
conda install rsem=1.3.0
```

- Download the genome and genome annotation files, verify `md5sum`s
```console
wget ftp://ftp.ebi.ac.uk/pub/databases/gencode/Gencode_human/release_27/GRCh38.primary_assembly.genome.fa.gz
wget ftp://ftp.ebi.ac.uk/pub/databases/gencode/Gencode_human/release_27/gencode.v27.primary_assembly.annotation.gff3.gz
wget ftp://ftp.ebi.ac.uk/pub/databases/gencode/Gencode_human/release_27/gencode.v27.primary_assembly.annotation.gtf.gz
wget ftp://ftp.ebi.ac.uk/pub/databases/gencode/Gencode_human/release_27/MD5SUMS
md5sum -c MD5SUMS 2>/dev/null | grep OK
```
`2>/dev/null` bit gets rid of the `standard error stream`, leaving only the `standard output stream`, which is the relavent output from `md5sum -c`.

- Prepare the genome
```console
rsem-prepare-reference \
--gtf gencode.v27.primary_assembly.annotation.gtf \
--star \
--star-path /DATA/anaconda3/envs/star_rsem/bin \
-p 8 \
GRCh38.primary_assembly.genome.fa \
my_genome
```

- Align & count reads
```console
for file in ...; \
do rsem-calculate-expression \
-p 8 \
--star \
--output-genome-bam \
--star-path /DATA/anaconda3/envs/star_rsem/bin \
--star-gzipped-read-file \
--forward-prob=0 \
$file \
/DATA/grch38/my_genome \
${file:11:7}; \
done

```
