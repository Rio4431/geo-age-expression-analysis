# GEO Age-Associated Gene Expression Analysis

A Jupyter notebook for exploring associations between age and gene expression using NCBI GEO microarray and bulk RNA-seq data.

## Features
- Select a GEO Series (GSE ID) and an NCBI Gene ID.
- Analyze age trends using OLS regression and Spearman correlation.
- Compare young and older groups using Welch's t-test.
- Export CSV results and plots.

## Usage
```bash
pip install -r requirements.txt
jupyter notebook geo_age_expression_analysis.ipynb
```

Set `GSE_ID` and `GENE_ID` in the notebook. Additional settings may be needed for some datasets. The `data/` and `results/` folders are created automatically.

## Note
Results are exploratory. Check sample metadata and expression units before interpreting findings. Not all GEO datasets are supported; RNA-seq analysis is not a substitute for count-based differential expression testing.

## Validation and limitations

This notebook is designed for exploratory analysis of a **specified gene**, not a genome-wide differential expression study.

- Verify that the GEO sample metadata describe chronological age for the samples selected, and that the analyzed specimens and study groups are comparable.
- Inspect the platform / gene annotations, expression scale, missing values, sample sizes, and distribution before interpreting OLS, Spearman correlation, or Welch's t-test.
- For bulk RNA-seq, distinguish raw counts, TPM/FPKM, and transformed expression measurements. The exploratory statistics here do not replace count-based differential expression tools such as DESeq2.
- Availability of expression matrices, Gene ID mappings, and sample metadata varies by GSE. Some studies require local files or manual configuration.
- This repository does not currently provide a documented cross-dataset benchmark demonstrating successful execution on a defined validation suite. Do not assume that every GEO Series is supported.

## Reproducibility checklist

1. Record the GSE accession, NCBI Gene ID, selection filters, age thresholds, expression source and scale.
2. Install dependencies from `requirements.txt` and run the notebook using the stated parameters.
3. Inspect the source sample metadata and exported results before drawing conclusions.
4. Record any local matrix files, manual mappings, exclusions, and transformations used.

The notebook and dependency list are public; GEO datasets remain subject to their own accessibility and annotation constraints.
