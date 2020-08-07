---
title: "Available Bioinformatics Services"
permalink: /service_details/
layout: single
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
---

## Whole Genome Sequencing Analysis Services

### Variant Analysis
For Variant Analysis workflows, samples will be aligned to the requested reference genome using an appropriate aligner (BWA/minimap2/Dragen) and variants called to VCF format. If applicable annotations are available, putative variant consequences will also be provided. 

Deliverables: 
- Input file QC
- Aligned BAM file
- Summary metrics for mapping
- VCF file
- Table of annotated variants
- Up to 3 follow up filtrations of variants

### DeNovo Assembly
For De Novo Genome Assembly, samples will be assembled using an appropriate assembler (Canu/miniasm/SPAdes) and checked for assembled quality. As this is often an iterative process, the investigator will be actively consulted to tune parameters for optimal assembly and include additional data. Prokaryotic assemblies will also include predictive gene annotation with Prokka. 

Deliverables:
- Input file QC
- De novo assembly quality metrics including BUSCO score
- FASTA output genome
- Annotation file (if applicable)

## RNA Sequencing Analysis Services

### Differential Gene Expression
For differential gene expresion, samples will be aligned to the requested reference genome using STAR aligner and differential gene expression shall be calculated using the DESeq2 method. 

Deliverables:
- Input file QC
- Aligned BAM file
- Pairwise Differential gene expression spreadsheet for conditions
- Global expression heatmap with standard hierarchal clustering
- Sample PCA plot
- Per comparison volcano plot
- Up to 10 focused heatmaps or custom plots

### Pathway Analysis
For pathway analysis, there are several options for tools:
- Ingenuity Pathway Analysis (IPA):
  - Rutgers OARC maintains a license for IPA. To gain access, contact Les Michelson in OARC. 
  - Once access is attained, MaGIC can generate the data within IPA and transfer the analysis to you. 
  - IPA provides gene enrichment analysis for their canonical pathways (Qiagen curated pathways), upstream regulators, and putative disease states, as well as cross sample comparisons and several networking tools. They also have some *in silico* discovery tools available. 
    - There is a maximum number of genes that can be inputted to IPA. Be cautious of subsetting too far and generating false positive information. 
- iPathway Guide:
  - MaGIC maintains a license for iPathway Guide. No special access is needed, just a [free account](https://apps.advaitabio.com/oauth-provider/register?referrer=website) associated with your preferred email address. 
  - MaGIC will generate the data within iPathway then share the analysis with your account email. 
  - iPathway provides gene enrichment analysis for their curated pathways, standard gene ontologies (GO), upstream regulators, and possible pertubation mechanisms, as well as cross sample meta-analysis and several networking tools. iPathway also provides a standard output report. 

For custom pathway analysis (such as GSEA), please contact the Core to discuss availability and deliverables. 

### Single Cell Analysis
For single cell analysis, samples will be deconvoluted and aligned using the 10X cellranger wrapper to the appropriate genome. Matrices will be inputed to the Seurat workflow for secondary processing. 

Additional options are available:
- Hash tag analysis
- CITE-seq analysis
- Pseudotime analysis (in development)
- Scanpy workflow (in development)

Deliverables:
- Cellranger output QC files
  - Loupe cell browser files
  - .h5 matrices
  - HTML QC
- QC for determining filtration
- UMAP clustering
- Spreadsheet for per-cluster markers (or conserved markers)
- Feature plots, violin plots, and ridge plots for top 6 markers per cluster
- Up to 20 follow up plots

## Epigenetics Sequencing Analysis Services

### Differential Peak Calling
For differential peak calling of either ChIP or ATAC data, reads will be aligned to the requested genome using the BWA aligner followed by peak calling using MACS2. Differential peak comparisons will be performed using the DESeq2 method. 

Deliverables: 
- Input file QC
- Aligned BAM file
- Pairwise Differential gene expression spreadsheet for conditions

## Amplicon Sequencing Services

### Unique Amplicon Counting
For unique amplicon counting, read pairs are stitched using Pandaseq followed by bash tools for counting unique read pairs. Specific primer sites can be trimmed on request. 

Deliverables: 
- Input file QC
- Spreadsheet for list of amplicons and count

### 16s Metagenomics
For 16s Metagenomics, samples will be converted into amplicon sequencing variants (ASVs) via DADA2 counting and analyzed through QIIME2 for taxonomic classifications and visualization. 

Deliverables: 
- Input file QC
- Abundance tables
- Alpha diversity
- Beta diversity
- Taxonomic assignment
- Diversity barplots by taxonomic rank

### VDJ Diversity
For VDJ diversity, samples will be processed through the [Immcantation](https://immcantation.readthedocs.io/en/stable/) pipeline. 

Deliverables:
- Input file QC
- Diversity analysis spreadsheet
- Up to 5 output plots
