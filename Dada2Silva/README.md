# DADA2 & Silva

Input: Illumina-sequenced paired-end fastq files that have been demultiplexed by sample and the barcodes/adapters have been removed. 

Output: amplicon sequence variant (ASV) table which is a higher-resolution analogue of the traditional OTU table which records the number of times each **exact amplicon sequence variant** was observed in each sample. Taxonomy is then assigned using the SILVA reference database and the data is combined into a phyloseq object.

## Some good resources for understanding the DADA2 pipeline

Our work flow is a mash-up of the following two tutorials: 

*Dada2 tutorial* https://benjjneb.github.io/dada2/tutorial.html

*Dada2 with Big Data* https://benjjneb.github.io/dada2/bigdata.html

## Before you start this example work flow:

### 1. Download example fastq files.
The files are in a [zipped folder.](https://drive.google.com/file/d/10vdRDtyg1WKvHH7NzHVy4spqH1XJhb0_/view?usp=sharing) on the google drive.

### 2. Create a folder in your forked repository called "fastqs" and move the individual fast q files into this folder.

### 3. Download the Silva databases used in the example.

The dada2 package GitHub maintains the most updated versions of the [Silva databases.](https://benjjneb.github.io/dada2/training.html). The versions used here in the example were last updated on March 10, 2021. You can download the files used in the example [here.](https://drive.google.com/file/d/1AKj1_DPgkQB7BS_4wDYARUpWQ5lC1FX9/view?usp=sharing)

## Other notes before running your own samples on DADA2:
- DADA2 should be run on each sequencing run/lane separately. Absolutely do not combine runs prior to running DADA2!
- If samples from the same project were sequenced on different runs/lanes, you can combine them right before the SILVA classification step, but no earlier.

