# Data Collection

This document goes over the process of acquiring the original data files for the project and processing them to get the format used in the publication.

## Data Sources

The source for the data is https://elifesciences.org/articles/73983. The inferred genotype and phenotype data is available for download here: https://datadryad.org/dataset/doi:10.5061/dryad.1rn8pk0vd.

## Steps

Download all of the files from https://datadryad.org/dataset/doi:10.5061/dryad.1rn8pk0vd and place them into a directory.

In order to have the same dataset used in the original publication the
- geno_data_1.txt.gz
- geno_data_2.txt.gz
- geno_data_3.txt.gz
- geno_data_4.txt.gz
- geno_data_5.txt.gz

files need to be combined into a single file. Then they need to converted into a numpy format using the script `convert_to_numpy.py`.

For example, let's saw we have all of the file in `example_data`. Then we would run the following commands:

```bash
cat example_data/geno_data_*.txt.gz > example_data/geno_data.txt.gz

python convert_geno_data.py -i example_data/geno_data.txt.gz -o example_data/merged_geno_data.npy
```
