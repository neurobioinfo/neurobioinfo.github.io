# FAQ and the Definitions of Terms Used in Neurobioinfo Core Facility Workflows

<!-- A Frequently Asked Questions (FAQ) section for a newly established Bioinformatics core facility will _de facto_ be a little scarce. In addition to some obvious questions, we also provide a short glossary of the terms that we are commonly using in our workflows and communications with you. -->

  

Please note that the links presented below are thought to be good resources but do not signify endorsements of the institution, or company presenting these definitions or tools.

  

Any suggestions for additions to any of our pages, but particularly this one, will be most welcome. Send them to [neurobioinfo@mcgill.ca](mailto:neurobioinfo@mcgill.ca).

  

# Frequently Asked Questions (FAQ):

  

Q001 - What is the best e-mail to use to contact you?<br>
A001 - [neurobioinfo@mcgill.ca](mailto:neurobioinfo@mcgill.ca)

  

Q002 - What is the best way to initiate a new project with the Neuro Bioinformatics Core Facility?<br>
A002 - Fill out the form [here](https://forms.clickup.com/f/c0qg2-87/ZA5RVAIEIX2YE3LHPV).

  

Q003 - Do I need to have some Compute Canada disk and/or compute allocation before I initiate a project with you?<br>
A003 - No. Actually good to talk to us before you initiate your project. Contact us at [neurobioinfo@mcgill.ca](mailto:neurobioinfo@mcgill.ca) or fill out the intake form [here](https://forms.clickup.com/f/c0qg2-87/ZA5RVAIEIX2YE3LHPV).
  

Q004 - Where do I go to get a Compute Canada account?<br>
A004 - After talking to us, here is the link to get started on that: [Compute Canada Account at McGill.](https://acelab.cbrain.mcgill.ca/doku.php?id=obtaining_a_compute_canada_account)

  

**Have more questions? Contact us at: [neurobioinfo@mcgill.ca](mailto:neurobioinfo@mcgill.ca)**

  


# Definitions

A short glossary of terms and resources used at the Neuro Bioinformatics Core Facility:


Commonly used Tags:

*   **Definition**
*   **File format**
*   **Ressource**
*   **Software**
*   **Wikipedia**

  

## Alignment metrics

*   **Ressource**
*   Also see: **Picard**
*   [Picard Alignment Metrics Definitions](https://broadinstitute.github.io/picard/picard-metric-definitions.html)
*   From PerkinElmer: [The five quality control (QC) metrics every NGS user should know](https://horizondiscovery.com/en/blog/the-5-ngs-qc-metrics-you-should-know)

## BAM

*   **File format**
*    **Wikipedia**: [Binary Alignment Map](https://en.wikipedia.org/wiki/Binary_Alignment_Map)
*   Also see: **SAM**
*   SAM and BAM file formats are meticulously detailed in the [SAM format specification](https://samtools.github.io/hts-specs/SAMv1.pdf) [document](https://samtools.github.io/hts-specs/SAMv1.pdf).
* **Definition**: A BAM file (.bam) is the binary version of a SAM file. A SAM file (.sam) is a tab-delimited text file that contains sequence alignment data. 
**Indexing**: IGV requires that both SAM and BAM files be sorted by position and indexed and that the index files follow a specific naming convention. 
[BAM | Integrative Genomics Viewer - Broad Institute](https://short.gy/wZoY8d)
*   From **YouTube**: [Understanding SAM/BAM file specifications](https://www.youtube.com/watch?v=tADZk2GsEaE)

## BED

*   **File format**
*   **Definition**: BED (Browser Extensible Data) format provides a flexible way to define the data lines that are displayed in an annotation track. 
*   [https://genome.ucsc.edu/FAQ/FAQformat.html#format1](https://genome.ucsc.edu/FAQ/FAQformat.html#format1)

## CNV

*   **Wikipedia**: [Copy number variation](https://en.wikipedia.org/wiki/Copy_number_variation)
*   **Definition**: A copy number variation (CNV) is when the number of copies of a particular gene varies from one individual to the next. Following the completion of the Human Genome Project, it became apparent that the genome experiences gains and losses of genetic material. [https://www.genome.gov/genetics-glossary/Copy-Number-Variation](https://www.genome.gov/genetics-glossary/Copy-Number-Variation)
*   Reference: Copy number variation in human health, disease, and evolution. Zhang F, Gu W, Hurles ME, Lupski JR.Annu Rev Genomics Hum Genet. 2009;10:451-81. PMID: [19715442](https://pubmed.ncbi.nlm.nih.gov/19715442/) 

## CRAM

*   **File format**
*   **Wikipedia**: [CRAM (file format)](https://en.wikipedia.org/wiki/CRAM_(file_format)#:~:text=CRAM%20is%20a%20compressed%20columnar,Map%20(BAM)%20file%20formats.)
*   **Definition**: CRAM is a compressed columnar file format for storing biological sequences aligned to a reference sequence, initially devised by Markus Hsi-Yang Fritz et al. CRAM was designed to be an efficient reference-based alternative to the Sequence Alignment Map (SAM) and Binary Alignment Map (BAM) file formats. (from [CRAM)](https://en.wikipedia.org/wiki/CRAM_(file_format)#:~:text=CRAM%20is%20a%20compressed%20columnar,Map%20(BAM)%20file%20formats.)
*   Original Reference: Efficient storage of high throughput DNA sequencing data using reference-based compression. Hsi-Yang Fritz M, Leinonen R, Cochrane G, Birney E. Genome Res. 2011 May;21(5):734-40. PMID: [21245279](https://pubmed.ncbi.nlm.nih.gov/21245279/) 


## FASTQ

*   **File format**
*   **Definition**: FASTQ format is a text-based format for storing both a nucleotide sequence and its corresponding quality scores (from [Wikipedia](https://en.wikipedia.org/wiki/FASTQ_format)).
*   From the [NCBI's File Format guide](https://www.ncbi.nlm.nih.gov/sra/docs/submitformats/): [FASTQ Files](https://www.ncbi.nlm.nih.gov/sra/docs/submitformats/#fastq-files)

## GVCF

*   **File format**
*   Also see: **VCF**
*   Also see **GATK**
*   **Definition**: GVCF stands for Genomic VCF. A gVCF is a kind of VCF, so the basic format specification is the same as for a regular VCF (see the spec documentation [here](http://vcftools.sourceforge.net/specs.html)), but a Genomic VCF contains extra information. The key difference between a regular VCF and a gVCF is that the gVCF has records for all sites, whether there is a variant call there or not. 
*   Genomic VCF (gVCF) extended format includes additional information about "blocks" that match the reference and their qualities.
*   From the GATK pages: [GVCF - Genomic Variant Call Format](https://gatk.broadinstitute.org/hc/en-us/articles/360035531812-GVCF-Genomic-Variant-Call-Format)
*   Broad Institute GitHub: [What is a GVCF and how is it different from a 'regular' VCF?](https://github.com/broadinstitute/gatk-docs/blob/master/gatk3-faqs/What_is_a_GVCF_and_how_is_it_different_from_a_'regular'_VCF%3F.md)

## GATK

*   **Software**
*   **Ressource**
*   **Definition**: A genomic analysis toolkit (GATK) is for identifying SNPs and indels in germline DNA and RNAseq data. Its scope is now expanding to include somatic short variant calling, and to tackle copy number (CNV) and structural variation (SV). GATK also includes many utilities to perform related tasks such as processing and quality control of high-throughput sequencing data, and bundles the popular Picard toolkit.
*   From the Broad Institute: [Genome Analysis Toolkit](https://gatk.broadinstitute.org/hc/en-us)
*   Original publication: The Genome Analysis Toolkit: a MapReduce framework for analyzing next-generation DNA sequencing data.McKenna A, Hanna M, Banks E, Sivachenko A, Cibulskis K, Kernytsky A, Garimella K, Altshuler D, Gabriel S, Daly M, DePristo MA.Genome Res. 2010 Sep;20(9):1297-303. PMID: [20644199](https://pubmed.ncbi.nlm.nih.gov/20644199/) 

## GWAS

*   **Definition**: A genome-wide association study (GWAS) is an approach used in genetics research to associate specific genetic variations with particular diseases. The method involves scanning the genomes from many different people and looking for genetic markers that can be used to predict the presence of a disease. (From the [NHGRI/NIH](https://www.genome.gov/genetics-glossary/Genome-Wide-Association-Studies))

## IGV

*   **Software**
*   [https://software.broadinstitute.org/software/igv/](https://software.broadinstitute.org/software/igv/)
*   From the IGV website: The **Integrative Genomics Viewer (IGV)** is a high-performance, easy-to-use, interactive tool for the visual exploration of genomic data. It supports flexible integration of all the common types of genomic data and metadata, investigator-generated or publicly available, loaded from local or cloud sources.
*   Quick IGV tutorial from [bioinformatics.ca](http://bioinformatics.ca): [YouTube Channel (15 minutes)](https://www.youtube.com/watch?v=ftG9vrHmjFg&list=PL3izGL6oi0S9B0xqTnu2adTt8v2XGu2zx&index=2):

## Mapping rate

*   Mapping rate is the “Uniquely mapped reads %”, which is defined as a proportion of uniquely mapped reads out of all input reads. For a very good library, it exceeds 90%, and for good libraries, it should be above 80%. (from PMID: [26334920](https://pubmed.ncbi.nlm.nih.gov/26334920/))
*   A reference: Mapping RNA-seq Reads with STAR. Dobin A, Gingeras TR. Curr Protoc Bioinformatics. 2015 Sep 3;51:11.14.1-11.14.19. PMID: [26334920](https://pubmed.ncbi.nlm.nih.gov/26334920/)

## miRNA

* **Wikipedia:** [microRNA](https://en.wikipedia.org/wiki/MicroRNA)
*   **Definition**: A microRNA (abbreviated miRNA) is a small single-stranded non-coding RNA molecule (containing about 22 nucleotides) found in plants, animals and some viruses, that functions in RNA silencing and post-transcriptional regulation of gene expression. miRNAs function via base-pairing with complementary sequences within mRNA molecules. As a result, these mRNA molecules are silenced, by one or more of the following processes: 
	1. Cleavage of the mRNA strand into two pieces
	2. Destabilization of the mRNA through shortening of its poly(A) tail,
	3. Less efficient translation of the mRNA into proteins by ribosomes.



## Picard

*   **Software**
*   **Definition**: A set of command-line tools (in Java) for manipulating high-throughput sequencing data and formats such as SAM/BAM/CRAM and VCF. (from [https://broadinstitute.github.io/picard/](https://broadinstitute.github.io/picard/))
*   [Picard GitHub source page](https://github.com/broadinstitute/picard)

## QC report

*   Quality Control output from various tools.
*   NGS raw data Quality Control report [explained by the Galaxy p](https://training.galaxyproject.org/training-material/topics/sequence-analysis/tutorials/quality-control/tutorial.html)[roject](https://training.galaxyproject.org/training-material/topics/sequence-analysis/tutorials/quality-control/tutorial.html).
*   Alignment QC in RNA-Seq [explained by the Griffith lab](https://rnabio.org/module-02-alignment/0002/06/01/Alignment_QC/).

## Reference Genome

*   **Definition**: A reference genome (also known as a reference assembly) is a digital nucleic acid sequence database, assembled by scientists as a representative example of the set of genes in one idealized individual organism of a species. ... Instead a reference provides a haploid mosaic of different DNA sequences from each donor. (From Wikipedia: [Reference genome](https://en.wikipedia.org/wiki/Reference_genome)).
*   Genome Reference Consortium: [Human reference Genome: GRCh38.p13 (latest minor release)](https://www.ncbi.nlm.nih.gov/grc/human)

## SAM

*   **File format**
*   Also see: **BAM**
*   **Definition**: Sequence Alignment Map (SAM) is a text-based format originally for storing biological sequences aligned to a reference sequence developed by Heng Li and colleagues (From **Wikipedia**: [SAM (File Format)](https://en.wikipedia.org/wiki/SAM_(file_format)#cite_note-samtools-1)).
*   [Sequence Alignment/Map Format Specification](https://samtools.github.io/hts-specs/SAMv1.pdf)
*   Original publication: The Sequence Alignment/Map format and SAMtools. Li H, Handsaker B, Wysoker A, Fennell T, Ruan J, Homer N, Marth G, Abecasis G, Durbin R; 1000 Genome Project Data Processing Subgroup. Bioinformatics. 2009 Aug 15;25(16):2078-9.  PMID: [19505943](https://pubmed.ncbi.nlm.nih.gov/19505943).

## Structural variations

*   Also see: **CNV**
*   **Definition**: Genomic structural variation is the variation in the structure of an organism's chromosome. It consists of many kinds of variation in the genome of one species and usually includes microscopic and submicroscopic types, such as deletions, duplications, copy-number variants, insertions, inversions and translocations. Originally, a structure variation affects a sequence length about 1kb to 3Mb, which is larger than SNPs and smaller than chromosome abnormality (though the definitions have some overlap). (from Wikipedia entry)
*   **Wikipedia**: [Structural variations](https://en.wikipedia.org/wiki/Structural_variation).
*   Structural variation in the human genome. Feuk L, Carson AR, Scherer SW. Nat Rev Genet. 2006 Feb;7(2):85-97. PMID: [16418744](https://pubmed.ncbi.nlm.nih.gov/16418744/)
*   **Reference:** Structural variant calling: the long and the short of it. Mahmoud M, Gobet N, Cruz-Dávalos DI, Mounier N, Dessimoz C, Sedlazeck FJ. Genome Biol. 2019 Nov 20;20(1):246. PMID: [31747936](https://pubmed.ncbi.nlm.nih.gov/31747936/)


## VCF
*   **File format**
*   Also see: **GVCF**
*   Also see: **GATK**
*   **Wikipedia**: [Variant Call Format](https://en.wikipedia.org/wiki/Variant_Call_Format).
*   **Definition**: The Variant Call Format (VCF) specifies the format of a text file used in bioinformatics for storing gene sequence variations. (from [Wikipedia](https://en.wikipedia.org/wiki/Variant_Call_Format)).
*   Broad Institute GitHub: [What is a GVCF and how is it different from a 'regular' VCF?](https://github.com/broadinstitute/gatk-docs/blob/master/gatk3-faqs/What_is_a_GVCF_and_how_is_it_different_from_a_'regular'_VCF%3F.md)
*   [The Variant Call Format and VCFtools](http://vcftools.sourceforge.net/VCF-poster.pdf)


##### End of page 

Want to see other entries? Send your suggestions to [neurobioinfo@mcgill.ca](mailto:neurobioinfo@mcgill.ca)!

