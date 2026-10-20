# GEO Skin Aging Analysis Template

A reusable Jupyter notebook for exploring age-associated gene expression in healthy human skin using the public NCBI GEO dataset [GSE18876](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE18876) (platform GPL5175).

## Features

- Select a target gene by **NCBI Gene ID**.
- Match gene annotations to microarray probe sets.
- Analyze age associations with OLS regression and Spearman correlation.
- Compare young and older groups using Welch’s t-test (95% confidence interval and nominal p-value).
- Export CSV summaries and PNG plots.

## Getting started

```bash
pip install -r requirements.txt
jupyter notebook geo_skin_aging_analysis.ipynb
```

Edit `GENE_ID`, `YOUNG_MAX`, and `OLD_MIN` in the configuration cell, then run all cells. GEO data are downloaded on first use to `data/`; outputs are saved under `results/`.

## Limitations

This notebook is tailored to GSE18876 / GPL5175, not all GEO datasets. RMA expression is typically on a log2 scale. Reported p-values are not adjusted for multiple testing; findings are exploratory and do not establish causality.

## Data source

NCBI Gene Expression Omnibus: [GSE18876](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE18876). Original dataset and annotations remain subject to their respective source terms.