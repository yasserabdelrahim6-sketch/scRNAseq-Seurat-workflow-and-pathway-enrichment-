
```markdown
# scRNA-seq Analysis Workflow

This repository provides a reproducible pipeline for single-cell RNA-seq (scRNA-seq) analysis using Seurat and related R packages.

## Features

- Data loading and merging for multiple 10X Genomics samples
- Quality control (QC) and filtering of cells and genes
- Normalization, cell cycle scoring, highly variable gene selection
- Dimensionality reduction (PCA/UMAP) and clustering
- Differential expression and marker analysis
- Pathway and gene set enrichment (GO, Hallmark, GSEA)
- Publication-ready figures and result tables as output

---

## Folder Structure

```
your-project-root/
├── data
│  
│  
│   
│   
├── write/
│   ├── figures/
│   └── tables/
├── scRNAseq_analysis.Rmd
└── README.md
```

---

## Getting Started

1. **Install packages in R:**

    ```r
    install.packages(c("tidyverse","Seurat","SCpubr","scater","purrr","clustree","SeuratDisk","enrichplot","msigdbr","EnhancedVolcano"))
    if(!requireNamespace("BiocManager")) install.packages("BiocManager")
    BiocManager::install(c("org.Mm.eg.db", "clusterProfiler"))
    ```

2. **Place your data** (10X sample folders, plus `cc.genes.mouse.rds`) inside the `data/` directory.

3. **Run the analysis**:
    - Open `scRNAseq_analysis.Rmd` in RStudio.
    - Edit data paths if necessary.
    - Click **Knit** to produce an HTML report.  
    - All figures and tables will be saved in `write/figures` and `write/tables`.

---

## Output

- **Figures:** `write/figures/`
- **Tables/CSVs:** `write/tables/`
- **HTML report:** Created by knitting `scRNAseq_analysis.Rmd`

---

