---
layout: page
title: Workdlows
permalink: workflows
---

#Workflows


On these pages, we describe the workflows we are currently offering as a service to our Neuro community. As described here, they are generic and we do adapt all of these on a case-by-case for each of our specific tasks.

For RNA and DNA sequence analysis, we will often refer to secondary or tertiary analyses in our discussions with you.  Here is what we are referring to, in part taken from Illumina documentation [1], and from Pereira and colleagues [2].

## Primary Analysis

The primary data analysis consists of the detection and analysis of raw data, targeting the generation of legible sequencing reads (base calling) and scoring base quality. The outputs from this primary analysis are FASTQ ﬁles and are often from the genome center that sequenced your samples, this is usually where we start, doing QC on your samples [2]. It is your responsibility to understand how data is generated. 

## Secondary Analysis

A secondary analysis will involve a per-sample alignment (mapping to a reference genome, and in 2021/2022, this is usually to the human reference hg38 (also known as GRCh38.p13 [3]) and then do a variant calling. This is typically the generation of a VCF file. This will include calling the various types of variation one can see in a genome: single nucleotide polymorphisms (SNP), small insertion/deletions (INDELS), less than 50 bp, larger structural INDELS (> 50bp), translocations/large deletions, Copy Number Variation (CNV) changes, and larger chromosomal aberrations like trisomies and the likes. 

## Tertiary Analysis

A tertiary analysis is everything that comes afterwards, starting with the joint-calling analysis step that allows better variant identification by leveraging population-wide information from cohorts [4]; annotations, filtering, some interpretation (this will be discussed with our team when planning your project). This is actually where a lot of the art of the trade will come into play, and where there will be more variation in the types of analysis we will perform, specific to your project and will inform the analysis we do to inform the functional impact of the variants you have identified in your analysis.

All of this will become clear after you have spoken to us, and a plan is set for the analysis we will be doing for you.

## Current workflows

This is a list of the current workflows we run in the Neuro Bioinformatics Core Facility. If you do not see the workflow you need, or if you want to use one of these or modify them, please do not hesitate to [contact us at neurobioinfo@mcgill.ca](mailto:neurobioinfo@mcgill.ca). 


* [RNA-Seq Analysis](/wf/rna)
* [RNA-Seq and Differential Expression Analysis](/wf/rna_dea)
* [miRNA-Seq Analysis](/wf/mirna)
* 
* [Whole-Genome/Exome Mapping and Variant Calling Analysis](/wf/wga)
* [Segregation Analysis](/wf/segregation)
* [Data Managemment](/wf/data_management)

## Bibliography

1. Illumina documentation [Software to help you focus on your research](https://www.illumina.com/informatics/sequencing-data-analysis.html)
2. Bioinformatics and Computational Tools for Next-Generation Sequencing Analysis in Clinical Genetics. Pereira R, Oliveira J, Sousa M. J Clin Med. 2020 Jan 3;9(1):132.  PMID: [31947757](https://pubmed.ncbi.nlm.nih.gov/31947757/) 
3. Genome Reference Consortium for the most recent human genome reference: [GRCh38.p13](https://www.ncbi.nlm.nih.gov/grc/human)
4. From the Broad's GATK documentation: [The logic of joint calling for germline short variants](https://gatk.broadinstitute.org/hc/en-us/articles/360035890431-The-logic-of-joint-calling-for-germline-short-variants)






