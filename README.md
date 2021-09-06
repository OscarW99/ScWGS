# ScWGS
### A WGS bioinformatics pipeline for validating CRISPR edits in Saccharomyces cerevisiae.
<br />

Genomic engineering of Saccharomyces cerevisiae has many applications from studying cellular function to producing synthetic chemicals. With the decreasing cost of sequencing, it is feasible to use whole genome sequencing for routine validation of engineered yeast strains. ScWGS is a bioinformatics pipeline for analysing yeast whole genome sequencing data. The pipeline takes paired-end, short-read data and combines several open-source bioinformatics tools to discover variants between query and reference haploid yeast genomes. ScWGS is packaged into a Docker container and all code is available in this repository. <br />
<br />

![ScWGS pipeline](https://github.com/OscarW99/ScWGS/blob/main/CRISPR%20validation%20pipeline.png?raw=true) <br />
<br />
ScWGS combines two methods of variant detection. The first is alignment of reads to a reference genome using bwa-mem [(Li 2013)](https://arxiv.org/abs/1303.3997) and then variant calling and variant annotation using [GATK haplotypecaller](https://gatk.broadinstitute.org/hc/en-us/articles/360037225632-HaplotypeCaller) and SnpEff [Cingolani et al. 2012](http://pcingola.github.io/SnpEff/se_introduction/) respectively.<br />
The second method uses the _Perfect Match Genomic Landscape_ (PMGL) algorithm [Palacios-Flores et al. 2018](https://www.pnas.org/content/118/14/e2025192118). This is a non-statistical solution to the analysis of variation in haploid genomes that decouples the identification of variants from their nature and location.
