# cell-ranger

Last updated: 2020-01-29

## Download & Installation

version: Cell Ranger - 3.1.0 (July 24, 2019), md5sum: a362d62530e9d6a653e5bad5b9c19aba

```console
wget -O cellranger-3.1.0.tar.gz "http://cf.10xgenomics.com/releases/cell-exp/cellranger-3.1.0.tar.gz?Expires=1580337014&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cDovL2NmLjEweGdlbm9taWNzLmNvbS9yZWxlYXNlcy9jZWxsLWV4cC9jZWxscmFuZ2VyLTMuMS4wLnRhci5neiIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTU4MDMzNzAxNH19fV19&Signature=SQtpHD3yOaCcSc5vfdirvPzQyT9-t44vS9qPSNDHtBLJ-000zKUJsiZffHtyyTvdEczYUuVSa85aOcI9WmaJ6feFKDrRYUT1FahATUSRLhTI5N~aPPKUpjnfgns1L8fe0UCCXQ~ErMuktR6iMRxn52TDxqwRGQloIf8TzJkY-I18zV~nZyt4O49dhdAqFwl9g854judvLw8eZ-RbyWoYi9Gia7DDT7BSCItrLqZOy-g9Nf0VgHwwfDN2LTzbSoJi-Uj73C-TQJor97Ylmp-eI4D4tew1rfhXuDGHsj4IYfnXYBhkLx-lJ~1bHJ5iJvtSLpOAetyq6shD5wO92ShgJg__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA"
# In case of "HTTP request sent, awaiting response... 403 Forbidden", escape the "&" right before "Key-Pair-Id=" with "\"
# or try with "curl".

md5sum cellranger-3.1.0.tar.gz 

tar -xzvf cellranger-3.1.0.tar.gz  
```

## Genome

Indexed GRCh38 from 10x (3.0.0, November 19, 2018), md5sum: edb1dc39a0e379e0f226ed9ee004be3c
```console
wget http://cf.10xgenomics.com/supp/cell-exp/refdata-cellranger-GRCh38-3.0.0.tar.gz

md5sum refdata-cellranger-GRCh38-3.0.0.tar.gz 

tar -xzvf refdata-cellranger-GRCh38-3.0.0.tar.gz 
```

Add the paths to the cell ranger and genome directories to `.bash_profile` and make a test run:

```console
cellranger testrun --id=tiny
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
