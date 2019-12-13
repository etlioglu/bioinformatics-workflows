# cell-ranger

Test

## Download & Installation

- version: Cell Ranger - 3.0.2 (January 15, 2019), md5sum: 73f3766579e800015f82daedb388fcd3

```console
wget -O cellranger-3.0.2.tar.gz "http://cf.10xgenomics.com/releases/cell-exp/cellranger-3.0.2.tar.gz?Expires=1576303594&Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cDovL2NmLjEweGdlbm9taWNzLmNvbS9yZWxlYXNlcy9jZWxsLWV4cC9jZWxscmFuZ2VyLTMuMC4yLnRhci5neiIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTU3NjMwMzU5NH19fV19&Signature=L-2VHxapKCgXSfIILxOIMYc0uhhAhIjck223sZHUDhgENGOmxS2gAlNqec2rZYO1NwrnPrwf~WfOWRFIbPS-5usQMxU2DBIRzl39hrb~OjE5Kd3tbQdJ8mk8sm89SJYJkZ2zQlT64KfRwT904vb8GGOlwBieGgoV~6k6V2ryW~g7cOXwE90pldXJpfPUqjjotna4GqhopxqH~5wXK5BSz814t961rt0Dvr7dUhzILEEQvC8lDS2xlDtxvRhqRdBGyhKcEQgDSXF30YUruhHiwrdwnyBgEm0BlOym9X79tPKk-UCGvlonOPsO0QjrvI8R~IxPKrrHBhtjk2l5lVPamA__&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA"

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
