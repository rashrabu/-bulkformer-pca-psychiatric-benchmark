# Data sources

## Primary MDD cohort

[GSE251778](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE251778): 169 participants, including 80 MDD cases and 89 controls. Peripheral blood leukocytes were isolated using LeukoLOCK. Sequencing protocols differ by sex. The notebook retrieves author-supplied count data from the pinned [multiomics_MDD source](https://github.com/INSERM-U1141-Neurodiderot/multiomics_MDD/tree/1d51753c1cfe444bbb14ee989fbaf5739ac39483).

Counts are converted to TPM using gene lengths, retaining the original 1,000-bp fallback for unmatched lengths, then transformed with ln(TPM + 1). The audit reports gene coverage and fallback counts.

## Exploratory psychiatric cohort

[GSE289146](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE289146): 299 PBMC samples, including 229 affected participants and 70 controls. This is a broader stress-related psychiatric phenotype, not an MDD-only cohort. The notebook reads RSEM TPM, strips Ensembl version suffixes, sums duplicate IDs, and applies ln(TPM + 1). It does not use the publication's covariate-corrected log2CPM matrix.

## Saved inputs

The original source notebook embeds predictions, 131-feature embeddings, and public study sample metadata. This public copy excludes that archive pending faculty sign-off and requires it as a separate local input. Sample IDs follow the source data; embeddings retain the original prediction-file order. Raw expression matrices are retrieved at runtime rather than committed. See [references](../references.md) for the publications.
