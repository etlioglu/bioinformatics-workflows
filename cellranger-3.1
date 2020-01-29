# cell-ranger

Test

## Download & Installation

- version: Cell Ranger - 3.0.2 (January 15, 2019), md5sum: 73f3766579e800015f82daedb388fcd3

```console
wget -O cellranger-3.0.2.tar.gz "http://cf.10xgenomics.com/releases/cell-exp/cellranger-3.0.2.tar.gz?Expires=1576303594&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cDovL2NmLjEweGdlbm9taWNzLmNvbS9yZWxlYXNlcy9jZWxsLWV4cC9jZWxscmFuZ2VyLTMuMC4yLnRhci5neiIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTU3NjMwMzU5NH19fV19&Signature=L-2VHxapKCgXSfIILxOIMYc0uhhAhIjck223sZHUDhgENGOmxS2gAlNqec2rZYO1NwrnPrwf~WfOWRFIbPS-5usQMxU2DBIRzl39hrb~OjE5Kd3tbQdJ8mk8sm89SJYJkZ2zQlT64KfRwT904vb8GGOlwBieGgoV~6k6V2ryW~g7cOXwE90pldXJpfPUqjjotna4GqhopxqH~5wXK5BSz814t961rt0Dvr7dUhzILEEQvC8lDS2xlDtxvRhqRdBGyhKcEQgDSXF30YUruhHiwrdwnyBgEm0BlOym9X79tPKk-UCGvlonOPsO0QjrvI8R~IxPKrrHBhtjk2l5lVPamA__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA"

# Alternatively:
curl -o cellranger-3.0.2.tar.gz "http://cf.10xgenomics.com/releases/cell-exp/cellranger-3.0.2.tar.gz?Expires=1576546780&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cDovL2NmLjEweGdlbm9taWNzLmNvbS9yZWxlYXNlcy9jZWxsLWV4cC9jZWxscmFuZ2VyLTMuMC4yLnRhci5neiIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTU3NjU0Njc4MH19fV19&Signature=ZhzP28d7qzqP6-6O3Hjx~PjquwBFYNrGrXNWkk2h-GJadnEC0v2ygwDLPOojEAH8aWuMZfiGmYA2mY2JqBO7QPC9oVNR-z2BKcm-hqtm20-GPn4cF3P5wAS4fsfMQFiS0dvgql~z7uLlKYMrrH~57AFRE2zPtSp8xk1i4S356A~A-STkKQiR4B4XQ3mmGUuv7D82uuH~dSYfA1JIvOQ1qU98nc5Lzw43ZMkQ8wwDgJjL26NG503bboraM3buvMbz290Cs7nZa5dsuaDfjJK92Bn10Zvch5NYOJjlDBRwgEyhuktMkCxFq1AllWavTZw9luD9RS1SxfGAG5rX9j5YYg__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA"

# In case of "HTTP request sent, awaiting response... 403 Forbidden", escape the "&" right before "Key-Pair-Id=" with "\"

md5sum cellranger-3.0.2.tar.gz

tar -xzvf cellranger-3.0.2.tar.gz 
```

## Genome

Indexed GRCh38 from 10x (1.2.0, November 16, 2016), md5sum: c3a4812f7fdb7ba84429a404ba478acf

```console
wget http://cf.10xgenomics.com/supp/cell-exp/refdata-cellranger-GRCh38-1.2.0.tar.gz

md5sum refdata-cellranger-GRCh38-1.2.0.tar.gz 

tar -xzvf refdata-cellranger-GRCh38-1.2.0.tar.gz 
```

Add the paths to the cell ranger and genome directories to `.bash_profile` and make a test run:

```console
cellranger testrun --id=tiny`
```

Example script 

```console
# Reference Genome
ref=/DATA/references/cell-ranger/refdata-cellranger-GRCh38-1.2.0

# Path to the main single cell directory
main_dir_path=/DATA/kul3_fasta/

# Single cell chemistry
chemistry=threeprime

for sample in ...
do

# Path to the fastq files
fastq_path=$main_dir_path/$sample

echo $sample

#NEXT seq only
cellranger count \
--id=${sample:0:9} \
--sample=$sample \
--transcriptome=$ref \
--fastqs=$fastq_path \
--chemistry=$chemistry \
--localcores=8 \
--localmem=64

rm ${sample:0:9}/outs/possorted_genome_bam.bam* # delete the resulting bam file and its index

done
```
