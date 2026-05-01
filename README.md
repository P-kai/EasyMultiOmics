# EasyMultiOmics

**EasyMultiOmics** is a user-friendly and comprehensive multi-omics analysis pipeline designed for integrated microbiome and resistome profiling. It provides streamlined workflows for short-read and long-read metagenomics, as well as single-cell microbial genomics, enabling researchers to perform end-to-end analyses from raw sequencing data to high-level biological insights.

The pipeline supports beginner-friendly yet robust analytical procedures and is suitable for diverse sequencing platforms, including second-generation (short-read) and third-generation (long-read) technologies.

---

## Key Features and Modules

### 1. Next-Generation Short-read Metagenomics
- Raw data quality control  
- Read-based taxonomic profiling  
- Read-based antimicrobial resistance gene (ARG) annotation  
- Metagenomic assembly  
- Metagenome binning  
- Bins quality assessment  
- Taxonomic annotation of bins  
- Metagenome-assembled genomes (MAGs) phylogenetic tree construction  

---

### 2. Nanopore Long-read Metagenomics (Refer to https://github.com/P-kai/EasyNanoMeta)
- Raw data quality control  
- Read-based taxonomic profiling  
- ARG annotation and quantification  
- Metagenomic assembly  
- Metagenome binning  
- Bins quality assessment  
- Taxonomic annotation of bins  
- MAGs phylogenetic analysis  

---

### 3. Hybrid Assembly and Analysis (Short-read and Long-read metagenomes)
- Hybrid metagenomic assembly  
- Metagenome binning  
- Bins quality assessment  
- Taxonomic annotation of bins  
- MAGs phylogenetic tree construction  

---

### 4. Single-cell Microbial Genomics
- Raw data quality control  
- Single amplified genome (SAG) assembly  
- SAG bins quality assessment  
- Taxonomic annotation  
- ARG annotation  
- Phylogenetic tree construction of SAGs  

---

### File descriptions
`Bins_analysis_results` contains all analysis results related to bins. `*_Checkm2-gtdbtk.xlsx` includes the bin quality-control table based on CheckM2-estimated completeness and contamination, the taxonomic classification table, bin size, contig N50, and other related information.
`*_bins_ARGs_ncbi_80_80.xlsx` contains the results of ARG identification in bins using ABRicate. The ABRicate parameters were set to a minimum coverage of 80% and a minimum nucleotide identity of 80%, and the database used was the NCBI AMRFinderPlus database.

`Taxonomic and ARGs composition` includes taxonomic classification results and antibiotic resistance gene (ARG) quantification results based on raw reads from short-read metagenomic sequencing, long-read metagenomic sequencing, and single-cell sequencing.

Taxonomic classification was performed using `Kraken2` with default parameters and the `k2_pluspfp` database.

ARG identification and quantification were performed using `ARGs_OAP` with default parameters and the `NCBI AMRFinderPlus` database.
