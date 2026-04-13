# AN_SRMeta_2026
The Role of the Gut Microbiome in Anorexia Nervosa: A Systematic Review and Integrative Meta Analysis
# Meta-analysis of Anorexia Nervosa microbiome datasets with SIAMCAT
This repository contains the R Markdown code knitted to HTML used for a meta-analysis of gut microbiome datasets in anorexia nervosa using SIAMCAT, including per-study association testing, pooled analysis, study-to-study transfer, leave-one-study-out validation, and descriptive diversity analyses.

## Main file

- `AnorexiaSysRevCode07042026.Rmd`

## Analysis overview

The R Markdown file performs the following main steps:

1. loads and harmonizes four microbiome datasets
2. constructs per-study SIAMCAT objects
3. performs univariate association testing
4. merges studies for pooled modeling
5. fits cross-validated LASSO models with SIAMCAT
6. evaluates study-to-study transfer and LOSO performance
7. runs meta-analytic linear mixed-effects models
8. performs descriptive alpha- and beta-diversity analyses
9. exports figures to image and PDF files

## Expected data structure

The code uses `here()` and expects the following folder structure relative to the project root:

```text
Metaanalysis/
├── Borgo_2017/
├── Mack_2016/
├── Prochazkova_2020/
└── Monteleone_2021/

The following input files are referenced in the R Markdown file. IMPORTANT: These files are available on request from the original authors and are not included in this repo!

Metaanalysis/Borgo_2017/ :
SraRunTable.csv
borgo2017meta.csv
res_idtaxa_genus.rds

Metaanalysis/Mack_2016/ :
Metadaten-Mack-neu.xlsx
mack2016meta.csv
Metadata_nachHeildelberg_Mai17_2024.xlsx
res_idtaxa_genus.rds

Metaanalysis/Prochazkova_2020/ : 
SraRunTable (5).txt
Table S5_formated.xlsx
res_idtaxa_genus.rds

Metaanalysis/Monteleone_2021/:
Clinical data anorexia samples.xlsx
res_idtaxa_genus.rds


Remark: Due to updates to R after the manuscript was finalized, the Rmd file may produce slightly different numerical results than those reported in the paper (differences may occur in the second decimal place).
