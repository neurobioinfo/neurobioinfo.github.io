---
layout: page
title: Whole-genome/exome mapping and variant calling Analysis
permalink: wf/segregation
---

# Segregation Analysis


![Segregation](/wf/Fig05_Variant_Segregation.jpg "Fig05_Variant_Segregation")

## Contents
- [Segregation Analysis]
- [Hail]
- [Steps of running]

## Segregation Analysis
This is a process to explore the distribution of genetic variants among families with <=2 phenotypes or disease states. This analysis breaks down counts of samples by genotype states (heterozygous reference, heterozygous, homozygous variant, no call), by disease status (affected vs nonaffected) and by family scope (in-family or global). **Each output line represents one variant in one family**. Additionally, since segregation analysis outputs are tab-separated, this program can be used to convert vcf to tabular format, including any user-defined annotations present in the input vcf file.

This program requires two inputs: 
1) a pedigree file with six tab-separated columns in the order:
* `familyid` 
* `individualid`
* `parentalid`
* `maternalid`
* `sex`	{1:male; 2:female, 0:unknown} 
* `phenotype`		{1: unaffected, 2: affected, -9:missing} 

as well as a single header line with the exact values above.

NOTE: if you wish to simply convert vcf to a tab-separated file, simply provide a pedigree file with only a single `familyid` and `phenotype`

2) Variant call data in vcf format (compressed with gzip/bgzip or uncompressed)

## Hail

The "seganalysis" Python module is developed on top of [Hail](https://hail.is/). Hail is a Python module built on the top of Apache Spark and serves as an open-source, scalable framework for genomic data manipulation and analysis. The seganalysis module was tested on [Spark-3.1.2, Pre-build for Apache Hadoop3.2](https://spark.apache.org/downloads.html).

## Steps of running pipeline 
The following steps show how to run the segregation pipeline.

#### Step 1: Run Spark 
First activate Spark on your system 
```
export SPARK_HOME=$HOME/spark-3.1.2-bin-hadoop3.2
export SPARK_LOG_DIR=$HOME/temp
module load java/11.0.2
cd ${SPARK_HOME}; ./sbin/start-master.sh
```

#### Step 2: Generate annotated file 
Run [VEP](https://useast.ensembl.org/info/docs/tools/vep/script/vep_tutorial.html) to generate the annotated file.   

#### Step 3:  Create hail matrixTable
Next, initialize hail and import your vcf file and write it as a matrix table, a data structure optimized to efficiently store and manipulate genomic data. In the code snippet below, we import a vcf file and write it as a `MatrixTable` file, then read the newly-created file into a MatrixTable object. The test data used below is available here: [https://github.com/The-Neuro-Bioinformatics-Core/seganalysis/test].

```
import sys
import pandas as pd 
import hail as hl
hl.import_vcf('./test/data/testseg.VEP.vcf',force=True,reference_genome='GRCh38',array_elements_required=False).write('./test/output/testseg.mt', overwrite=True)
mt = hl.read_matrix_table('./test/output/testseg.mt')
```

#### Step 4: Run the seganalysis module
```
from seganalysis import seg
ped = pd.read_csv('./test/data/testseg.ped', sep='\t')
destfolder = './test/output'
vcffile = './test/data/testseg.VEP.vcf'
seg.segrun(mt, ped, destfolder, hl, vcffile)    
```
This will generate two files: `header.txt` and `finalseg.csv`, in the  `destfolder`. `header.txt` includes the header of information in `finalseg.csv`. Columns of `finalseg.csv` are organized into the following sections:  1) locus and alleles, 2) CSQ, 3) Global- Non-Affected 4) Global-Affected,  5) Family, 6) Family-Affected 7) Family - Non-affected.  

##### locus and alleles
locus: chromosome and position <br/>
alleles:  REF allele and ALT allele(s)
##### CSQ
VEP places all annotations within the "CSQ" vcf INFO field. Running `seg.segrun()` will split CSQ into tab-separated columns.  
##### Global - Non-Affected
glb_naf_wild:  Global - Non-Affecteds, wildtype<br/>
glb_naf_ncl:     Global - Non-Affecteds, no call  <br/>   
glb_naf_vrt:     Global - Non-Affecteds, with variant    <br/>
glb_naf_homv:    Global - Non-Affecteds, homozygous for ALT allele<br/>
glb_naf_altaf:   Global - Non-Affecteds, ALT allele frequency   <br/>
##### Global - Affected
glb_aff_wild: Global - Affecteds, wildtype <br/>
glb_aff_ncl:     Global - Affecteds, no call    <br/> 
glb_aff_vrt:     Global - Affecteds, with variant  <br/>
glb_aff_homv:    Global - Affecteds, homozygous for ALT allele<br/>
glb_aff_altaf:   Global - Affecteds, ALT allele frequency   <br/>
##### Family
{famid}_wild: Family - all: wildtype <br/>
{famid}_ncl: Family - all: no call<br/>
{famid}_vrt: Family - all: with variant<br/>
{famid}_homv: Family - all: homozygous for ALT allele<br/>
##### Family - Affected
{famid}_wild_aff: Family - Affecteds: wildtype <br/>
{famid}_ncl_aff: Family - Affecteds: no call<br/>
{famid}_vrt_aff: Family - Affecteds: with variant<br/>
{famid}_homv_aff: Family - Affecteds: homozygous for ALT allele<br/>
##### Family - Nonaffected   
{famid}_wild_naf: Family - Nonaffecteds: wildtype <br/>
{famid}_ncl_naf: Family - Nonaffecteds: no call<br/>
{famid}_vrt_naf: Family - Nonaffecteds: with variant<br/>
{famid}_homv_naf: Family - Nonaffecteds: homozygous for ALT allele<br/>

#### Step 5 (optional): Cleanup and parsing
`finalseg.csv` can be cleaned up into a more excel-friendly format, better-suited to use excel column filters. Additionally, unwanted output columns can be removed by subsetting the `header.txt` file into a new file containing only the desired output columns (`header_need.txt` in the code snippet below). To clean without removing columns, simply use the original `header.txt` file instead.

```
from seganalysis import parser
header_need = './test/data/header_need.txt'
parser.sub_seg(destfolder, header_need)  
```
The final output of this step is the file `finalseg_modified.csv`

#### Step 6  Shut down spark  
Do not forget to deactivate environment and stop spark: 
```
cd ${SPARK_HOME}; ./sbin/stop-master.sh
```

## Bibliography:
1. [Hail-Powered Science. An incomplete list of scientific work enabled by Hail](https://hail.is/references.html).
