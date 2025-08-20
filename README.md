# ccpm-exome-freeze-qc
The two jupyter notebooks in this repo, contain the code used to qc and merge the CCPM exome freeze3 files. 

# 01_freeze3_exome_QC.ipynb
* converts VCF chunks to chromosome MTs (matrix tables)
* annotates variants in padded target intervals (target intervals not publicly available)
* removes multialleleic sites > 6
* splits multialleleic sites
* filter by genotype quality
* repartition and save as MT
* generates sample QC metrics by chromosome

# 02_merge_chromosomes.ipynb
* remove column data and generate vcf for annotation
* exports filtered genetic data to plink for PCA and major continental ancestry estimates
* exports merged vcf
