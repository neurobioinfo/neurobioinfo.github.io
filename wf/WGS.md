---
layout: page
title: Whole-genome/exome mapping and variant calling Analysis
permalink: wf/WGS
---

# Whole-genome/exome mapping and variant calling Analysis


![WGS](/wf/WF05_WGS_ver05.jpg "WGS")


## Secondary analysis of WGS DNAseq data using Illumina DRAGEN

Secondary analysis of whole-genome sequencing (WGS) or whole-exome sequencing (WES) is currently commonly performed at the Neuro Bioinformatics Core Facility and requires some input from the users about where the input files are, and what annotations are necessary. Some care should also be given to the control samples you want to use or have available in your own study.

* Short description of the workflow and its purpose:

* Run full per-sample secondary analysis pipeline on Illumina DRAGEN Bio-IT, via cloud-based Illumina Connected Analytics (ICA) platform.

* Generates per-sample: 
  * Alignment
  * small variant calls
  * Copy-Number Variant (CNV) calls
  * Structural Variant (SV) calls
  * Repeat expansions
  * Per-chromosome ploidy calls
  * Runs of heterozygosity
  * Various QC metrics
* Raw samples sequences are uploaded to ICA, passed through the Dragen Germline pipeline, then outputs are downloaded back to Compute Canada HPC (beluga server).

## Bibliography:

1. Original Link where workflow was first presented: Illumina [DRAGEN DNA Pipeline](https://support.illumina.com/content/dam/illumina-support/help/Illumina_DRAGEN_Bio_IT_Platform_v3_7_1000000141465/Content/SW/Informatics/Dragen/GPipelineIntro_fDG.htm)
2. Reliable variant calling during runtime of Illumina sequencing. Loka TP, Tausch SH, Renard BY. Sci Rep. 2019 Nov 11;9(1):16502 PMID: [31712740](https://pubmed.ncbi.nlm.nih.gov/31712740/) (This publication is not from Illumina, but it represents an early publication that references DRAGEN.)
3. From the GATK portal: [DRAGEN-GATK – GATK](https://gatk.broadinstitute.org/hc/en-us/articles/360045944831)

