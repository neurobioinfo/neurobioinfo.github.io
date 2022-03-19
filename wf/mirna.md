---
layout: page
title: miRNA-Seq Analysis
permalink: wf/mirna
---

# miRNA-Seq Analysis


![miRNA-Seq Analysis](/wf/WF03_miRNASeq_workflow_ver03.jpg "miRNASeq Analysis")


## miRNA-Seq, gene product abundance and discovery.

A microRNA (abbreviated miRNA) is a small single-stranded non-coding RNA molecule (containing about 22 nucleotides) found in plants, animals and some viruses, that functions in RNA silencing and post-transcriptional regulation of gene expression. miRNAs function via base-pairing with complementary sequences within mRNA molecules. As a result, these mRNA molecules are silenced, by one or more of the following processes: (1) cleavage of the mRNA strand into two pieces, (2) destabilization of the mRNA through shortening of its poly(A) tail, and (3) less efficient translation of the mRNA into proteins by ribosomes. (Definition from Wikipedia: microRNA) [1]

### Short description of the workflow and its purpose:
This workflow takes as input miRNA sequence reads (presumably with Unique Molecular Identifiers (UMIs))  in FASTQ format and uses a number of tools to QC, trim, map, analyze, count and do a differential gene expression depending on your experimental design. All of these tools and workflow were extracted from the Potlaab and colleagues publication[2]. Other details on Bioinformatic Analysis of MicroRNA Sequencing Data are also described in the publication from Fu and Dong [3].



### Tools used in this workflow:

a. [Fastqc](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)<br>
b. [UMI-tools](https://github.com/CGATOxford/UMI-tools)<br>
c. [Cutadapt](https://cutadapt.readthedocs.io/en/stable/guide.html)<br>
d. [Bowtie1](http://bowtie-bio.sourceforge.net/index.shtml)<br>
e. [Custom scripts \[1\]](https://www.sciencedirect.com/science/article/pii/S266591312030131X)<br>
f. [Samtools](https://www.htslib.org) + [RNAseqc](https://software.broadinstitute.org/cancer/cga/rna-seqc)<br>
g. [miRDeep2](https://github.com/rajewsky-lab/mirdeep2)<br>
h. [Custom scripts \[3\]](https://www.sciencedirect.com/science/article/pii/S266591312030131X)<br>
i. [Deseq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html) + [Edger2](https://bioconductor.org/packages/release/bioc/html/edgeR.html)<br>


## Bibliography:

1. Wikipedia entry for microRNA: https://en.wikipedia.org/wiki/MicroRNA
2. Pratibha Potlaab, Shabana AmandaAli, Mohit Kapoor A bioinformatics approach to microRNA-sequencing analysis https://www.sciencedirect.com/science/article/pii/S266591312030131X
3. Bioinformatic Analysis of MicroRNA Sequencing Data. Fu X, Dong D. Methods Mol Biol. 2018;1751:109-125. PMID: 29508293 and as a PDF on ResearchGate
