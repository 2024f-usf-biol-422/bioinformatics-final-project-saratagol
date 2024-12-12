# README for Variant Calling Pipeline for SARS-CoV-2 using Illumina short reads

Parts of this pipeline approach are based on the pipeline described in the [Data Carpentry Genomics lessons](https://datacarpentry.org/genomics-workshop/), which are made available under a [CC-BY 4.0 license](https://creativecommons.org/licenses/by/4.0/).

# Sara Tagol 
# sptagol@usfca.edu 
# Monday, November 25, 2024

# Bioinformatics Final Project: SARS-CoV-2 Sequencing from Experimentally Infected Hamsters and Ferrets

## Overview
This project focuses on analyzing sequencing data from SARS-CoV-2 infections in hamsters and ferrets. The dataset includes raw sequence reads from experiments that explored the effects of Paxlovid and Molnupiravir treatments on SARS-CoV-2 WA1, Delta, and Omicron variants. The analysis aims to assess the sequencing data quality, perform variant calling, and generate meaningful insights from the results using the provided bioinformatics pipeline.

## SRA Bioproject Information
- **Bioproject ID**: PRJNA894555
- **Data Type**: Illumina raw sequence reads
- **Scope**: Multispecies, focusing on SARS-CoV-2 variants in treated and untreated experimental groups
- **Data Size**: Approximately 100 GB (33055 MB)

## Analysis Steps
1. **Data Acquisition**:
   - Download sequencing data (FASTQ files) from the SRA Bioproject PRJNA894555.

2. **Data Quality Control**:
   - Run `FastQC` on all FASTQ files to assess sequencing quality.
   - Use `Trimmomatic` or similar tools to remove low-quality reads and adapter sequences.

3. **Read Alignment**:
   - Align the trimmed reads to the SARS-CoV-2 reference genome using `BWA` or `Bowtie2`.

4. **Variant Calling**:
   - Use `samtools` and `bcftools` to identify variants.
   - Filter and annotate the variants using tools such as `vcfanno` or `snpEff`.

5. **Quantitative Analysis**:
   - Compare variants across different experimental conditions (treated vs untreated).
   - Perform statistical analyses to identify significant differences in mutation patterns.

6. **Visualization**:
   - Generate graphs and plots using `ggplot2` in R, including:
     - Quality metrics for sequencing data
     - Variant distribution plots
     - Comparative mutation rates

7. **Documentation**:
   - Compile the results into an RMarkdown report, ensuring reproducibility.

## Other Information
- **Updates Log**:
  - *[11/25/2024]*: Project setup and initial data exploration completed.

## Notes
- Ensure all scripts are properly documented and follow best practices.
- The data analysis is executed on a remote server using the Linux command line, leveraging tools such as `FastQC`, `samtools`, `bcftools`, and R.
- I used ChatGPT to assist with explanation on code errors 

---