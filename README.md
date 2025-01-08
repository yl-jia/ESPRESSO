# ESPRESSO
All details 

## 1_info_table
- Meta data for single cell;

- UMAP coordinates;

- Cytotrace score.

## 2_stress_gene_info
- Two methods used for stress check;

- Geneset_1 is stress geneset extracted from MSigDB, see .xlsx for details;

- Genes_2 includes  6 stress genes, from paper < https://pubmed.ncbi.nlm.nih.gov/33947848/ >, single gene used for stress check;

I prefer Geneset_1 stress check, both merge and split plot available.

> In the feature_plot, KRT14 serves as a positive control for expression levels, compared to the low expression of stress-related genes.

## 3_geneset_enrichment_info

For linking organelle dye-based features with gene-based scRNA-seq, we first transformed the gene expression data into function-based geneset enrichment scores (using ssGSEA as implemented in the [*escape*](https://www.bioconductor.org/packages/release/bioc/html/escape.html) Bioconductor *package*). This transformation replaces the gene count matrix with single-cell function enrichment matrix, which includes four assays: “GO_CC”, “GO_BP”, “GO_MF,” and “Hallmark”. 

Gene sets were obtained from [human MSigDB collections](https://www.gsea-msigdb.org/gsea/msigdb/genesets.jsp).

The used genesets are given in `code_for_plot.pdf`

> There is no need to provide the gene list for the signatures used, as they are well-known and readily available in MSigDB.

## 4_selected_matrix_and_plot

Updated selected Hallmarks and BP matrix.

## code_for_plot.pdf

All code for new plot focusing on "Chromatin organization" and "Lysosome acidity"

> The stress gene(set) plot was replotted using true value instead of scaled score, which is better to assess the general stress level.

