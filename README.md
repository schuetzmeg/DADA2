# DADA2 tutorial
DADA2 analysis of pumice rock samples. This tutorial is designed for evaluating the relative abundance of phyla and orders in pumice rock samples using DADA2, Phyloseq, and ggplot. The first half of the tutorial occurs within dada2 and the second half uses phyloseq to further analyze.

### Usage 
- to manipulate and analyze raw sequencing data from 16S amplicon sequencing datafiles
- produce tables and plots about the sequenced samples to understand the sequencing results better 

### Input files:
- files to be input into this pipeline should contain the extensions `.fastq`
- there should be a forward and reverse file for each sample that was sequenced
- note any difference in file name format compared to the examples in this pipeline and change the copied code according to your input file format so the pipeline can understand your file organization

A few notes:
- make sure set your working directory so all files for input and outputs of the pipeline are organized in one place
- there is a pause step noted within the tutorial, if you need to pause the tutorial make sure you get to this step to save your progress
- when working with phyloseq make sure the files are in matrix format so that phyloseq can interpret and when finished using phyloseq use psmelt function to return files as dataframes that can be interpreted by ggplots for graphing results 

### Dependencies:
- This is an R script, need to execute this code in R or R studio. I used R studio when running this pipeline. 
- Need to download and load to analyze and manipulate data
```{r}
library(dada2)
library(phyloseq)
library(Biostrings)
library(ggplot2)
library(RColorBrewer)
library(tidyverse)
```

### External files needed 
`(Silva database files for taxonomic alignments)[https://zenodo.org/records/14169026]'

### Output files 
- csv files of raw numerical data
- ggplot plots for abundance (Phyla and Order)


# Contact
Please Contact Megan Schuetz with any questions or concerns at schuetzmeg6601@gmail.com
