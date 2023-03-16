# 2023-03-16-Intro-to-genomics-and-viral-data-analysis
Instructor: Grace E. Seo

Date: March 16, 2023

Website: https://mmid-bioinformatics-workshop.github.io/

**YouTube: **

If you have any questions, feel free to ask during the workshop in-person or online!

We look forward to seeing you there!


### The goal of this workshop is to teach the following topics:
1. Review tool installation using conda
2. What are some methods used to analyze viral genomics data?
3. (Workshop specific) What is nanopore sequencing?
4. (Workshop specific) Brief overview of King et al., 2020 paper (doi: https://doi.org/10.1186/s12879-020-05367-y)
5. (Workshop specific) How to analyze nanopore fastq files from King et al., 2020 using conda environments.

*For more practice, use the following dataset*
Since these are illumina data, use the following tools. 
[Viehweger et al., 2019 - reference paper](https://doi.org/10.1101%2Fgr.247064.118)
1. fastqc
2. bowtie2
3. samtools

***

Refer to the previous workshop materials! https://github.com/mmid-bioinformatics-workshop/

To access Conda materials --> [Introduction to Conda and Tool installation](https://github.com/mmid-bioinformatics-workshop/2023-03-09-Intro-to-Conda-and-Tool-installation)
&nbsp;

To access Jill's detailed Conda guide --> [2022 Introduction to Conda](https://github.com/MMID-coding-workshop/2022-01-19-Introduction-to-CONDA)



##  Required conda tool packages for the workshop

[fastqc v0.12.1](https://anaconda.org/bioconda/fastqc)
&nbsp;
[nanoplot v1.41.0](https://anaconda.org/bioconda/nanoplot)
&nbsp;
[minimap2 v2.24](https://anaconda.org/bioconda/minimap2) - in lieu of [bowtie2](https://anaconda.org/bioconda/bowtie2)
&nbsp;
[samtools v1.16.1](https://anaconda.org/bioconda/samtools)


## Required software for the workshop
[Integrated Genomics Viewer (IGV v2.16.0)](https://software.broadinstitute.org/software/igv/download)


***

## NOTE: if you are having an issue with installing tool packages in conda 

The problem may arise if you didn't configure necessary conda channels (especially samtools).

**Follow the instruction below to configure channels:**

1. Open Ubuntu terminal.

2. Check the list of conda channel. If this is your first time installing conda environment, you might only have default channel. 

`conda config --show channels`

3. Add conda channels in following order (channels must be added in the same as listed here).

`conda config --add channels conda-forge`
`conda config --add channels bioconda`

4. Check the conda channels again. Channels should appear in the following order.

`conda config --show channels`

```
bioconda
conda-forge
defaults
```

5. If conda channels are in the wrong order, remove them and add again. Top of the list is the most important channel.

`conda config --remove channels CHANNELNAME`

6. Update problematic conda tool package. (i.e. samtools)

`conda update --yes --channel bioconda samtools`


***

If you have any questions, feel free to ask during the workshop in-person or online!

We look forward to seeing you there!


