# ScWGS
### A WGS bioinformatics pipeline for validating CRISPR edits in Saccharomyces cerevisiae.
<br />

Genomic engineering of Saccharomyces cerevisiae has many applications from studying cellular function to producing synthetic chemicals. With the decreasing cost of sequencing, it is feasible to use whole genome sequencing for routine validation of engineered yeast strains. ScWGS is a bioinformatics pipeline for analysing yeast whole genome sequencing data. The pipeline takes paired-end, short-read data and combines several open-source bioinformatics tools to discover variants between query and reference haploid yeast genomes. ScWGS is packaged into a Docker container and all code is available in this repository. <br />
<br />

![ScWGS pipeline](https://github.com/OscarW99/ScWGS/blob/main/CRISPR%20validation%20pipeline.png?raw=true) <br />

ScWGS combines two methods of variant detection. The first is alignment of reads to a reference genome using bwa-mem [I'm an inline-style link](https://www.google.com) and then variant calling and variant annotation using GATK haplotypecaller [I'm an inline-style link](https://www.google.com) and SnpEff [I'm an inline-style link](https://www.google.com) respectively.<br />
The second method uses the _Perfect Match Genomic Landscape_ (PMGL) algorithm [I'm an inline-style link](https://www.google.com). This is a non-statistical solution to the analysis of variation in haploid genomes that decouples the identification of variants from their nature and location.
