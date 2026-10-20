# Reproducibility and provenance

## What was preserved and changed

The source is the supplied fully executed `BulkFormer_All_Additional_Analyses_v2_reviewed(2).ipynb`. Markdown was shortened. All statistical code and saved statistical outputs are preserved. The public-release loader was changed from an embedded base64 ZIP to a required local ZIP; its execution count and output were cleared. Two saved JavaScript download outputs were removed. No statistical analysis or revised loader was rerun during repository preparation.

The final supplied PNG/PDF figures were retained byte-for-byte. The primary poster PDF is the newly supplied original PDF, an 11-by-8.5-inch page with margins. A separate 40-by-30-inch export from the supplied tenth-draft PowerPoint is retained. See figure_reproduction.md for provenance.

## Reproduction boundary

This is downstream analysis from saved BulkFormer embeddings, not a verified end-to-end embedding-generation release. The original input archive is withheld from this public package pending faculty sign-off. The source notebook contains that archive, so the original unedited notebook must also stay out of the public upload until reviewed.

Required original archive SHA-256:
`cc233d28eac90e0e635618a61ffde2b11a678bdeb741349192ef1d50a4a672f1`

BulkFormer source commit: `5bcf5b99e799cd55f41e4d6fe8200b2cdf3d9589`.
MDD source commit: `1d51753c1cfe444bbb14ee989fbaf5739ac39483`.
Vocabulary: 20,010 genes; observed genes: 19,271 MDD and 19,894 PBMC.
Five repeat seeds: 20260921 through 20260925. Bootstrap: 5,000 draws, seed 20261009.

The install cell pins scikit-learn 1.8.0 and rdata 1.1.0. Other packages are not fully locked. A clean-environment rerun has not been verified.

## Rerun with approved local inputs

1. Download the public notebook and open it in Google Colab with a CPU runtime.
2. Obtain the original saved-input archive from the project team through an approved channel. It must contain both cohort folders at its root, not an extra enclosing folder.
3. Upload it through Colab's Files panel. Set `ORIGINAL_ARCHIVE_PATH` in section 1 to its actual path. The example path is `/content/BulkFormer_original_saved_inputs.zip`.
4. Run the configuration and install cells, then section 1. The hash must match; do not remove the check to accept a different archive.
5. Run remaining cells in order. `RUN_FULL_ANALYSES=True` runs repeated nested CV; `False` still requires the saved inputs and runs only the available original-prediction analyses.
6. Keep the exported results archive private pending review: it includes participant-level predictions and embeddings.

## Distinguish result sets

Section 9 contains historical transcribed estimates, not final poster estimates. Original single-partition bootstrap results are distinct from repeated-CV means. The reconstructed first mixed-cohort repeat differs slightly from the archived original predictions. Do not combine those as identical runs.

The supplied final2 figure-layout notebook is now included, alongside the board-layout alternative. Neither has saved outputs; they were not rerun. Their required original aggregate CSV exports are still missing. Complete repeated-CV predictions and the full run manifest were not supplied separately. Aggregate tables here were extracted from genuine saved displays and retain their displayed precision.
