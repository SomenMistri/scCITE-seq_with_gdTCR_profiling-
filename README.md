# Single-cell CITE-seq with γδTCR Repertoire Profiling

This GitHub repository contains a pipeline for analyzing single-cell CITE-seq data with TCR repertoire profiling of γδ T cells.

## Introduction

Single-cell CITE-seq (Cellular Indexing of Transcriptomes and Epitopes by sequencing) combined with γδTCR (gamma delta T-cell receptor) repertoire profiling allows for biological replicate pooling and simultaneous profiling of gene expression, surface proteins, and T-cell receptor sequences at the single-cell level. This repository provides a comprehensive pipeline to process, demultiplex, analyze, and visualize these multi-omics data.
_Note:This repository focuses on analysis of datasets generated by the 10x Genomics chromium 5' V1.1 kit._

## Pipeline Overview

### Step 1: [**Generate count matrix from sequence reads**](/vignettes/1_Reads_to_Count_matrix.md)
This step involves converting raw sequence reads (GEX, CSP, and VDJ)into a count matrix that represents the gene expression profile of individual cells.

### Step 2: [**Custom Cellranger VDJ data processing**](/vignettes/2_custom_TCR_VDJ_data_processing.md)
Performing custom analysis specifically on TCR sequences to generate a specialized matrix for downstream analysis using Seurat.

### Step 3: [**Make seurat object, filter cells, and demultiplex the hashtags**](/vignettes/3_QC_filter_and_demux.md)
Integrating different omics data, filtering cells based on quality metrics and demultiplexing the hashtags to separate the pooled biological replicates.

### Step 4: [**Data normalization, clustering, and basic visualization**](/vignettes/4_Normalization_clustering_BasicViz.md)
Integrating different omics data, normalizing, clustering cells based on similarities, and providing initial visualizations for basic exploration.

### Step 5: [**Cluster frequency comparison**](/vignettes/5_cluster_freq_comparison_between_samples.md)
Comparing cluster frequencies across different clusters between experimental groups to identify variations or similarities.

### Step 6: [**pseudo-bulk DGE analysis**](/vignettes/6_pseudo-bulk_DGE_analysis.md)
Performing pseudo-bulk differential gene expression analysis utilizing the power of multiple biological replicates per group.

### Step 7: [**Cell surface protein visualization**](/vignettes/7_ADT_protein_visualization.md)
Visualizing cell surface protein expression profiles on identified clusters or cell types.

### Step 8: [**TCR V-segment usage**](/vignettes/8_TRGV_TRDV_usage.md)
Analyzing and visualizing TCR V-segment usage patterns across different cellular clusters.

### Step 9: [**TCR CDR3aa analysis**](/vignettes/9_TCR_CDR3_analysis.md)
Analyzing and visualizing TCR CDR3 sequences to study the diversity and composition of the TCR repertoire.

This concludes the overview of the single-cell CITE-seq with γδTCR Repertoire Profiling pipeline.
