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
