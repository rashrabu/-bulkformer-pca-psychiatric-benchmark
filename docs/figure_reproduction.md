# Figure notebooks and reproduction

Use [02_poster_figures.ipynb](../notebooks/02_poster_figures.ipynb), based on the supplied `BulkFormer_Poster_Figures_final2(1).ipynb`. Its four final canvas sizes match the existing figure PDFs: paired repeats 12 x 5.3 inches; original differences 12 x 3.9; combined sensitivity with six methods 12 x 7.2; separate-sex intervals 12 x 7.0.

The supplied [board variant](../notebooks/alternatives/03_poster_figures_board.ipynb) is retained as an alternative layout. Both supplied figure notebooks have no saved execution outputs. Matching dimensions supports selection of final2; exact regeneration has not been tested without the original complete aggregate CSV exports. Existing final PNG/PDF figures are retained unchanged.

## Required saved aggregate tables

- `repeated_metrics.csv`: cohort, method, seed and AUROC for each repeat.
- `original_conditional_bootstrap.csv`: original-partition estimates and conditional bootstrap intervals.
- `separate_sex_conditional_bootstrap.csv`: intervals for separately trained sex-specific models, not pooled-model subgroup scores.
- `pca_plus_covariates_metrics.csv`: required to reproduce the final six-row combined sensitivity panel. Without it the code can omit that method.

The full-precision original files were not supplied separately. Do not manufacture them from rounded displays. These are aggregate exports; participant-level predictions and embeddings are not required to draw these figures.

## Run

In Colab, run the figure notebook cells in order and upload the four CSVs when prompted. Outside Colab, install numpy, pandas, matplotlib and IPython, set INPUT_PATHS to the four file paths, and execute in order. The export cell offers a download in Colab. Use the separate-sex table with the exact name or the correct analysis label. Do not mix different runs or upload historical-reference tables.

The notebook checks repeat counts, seeds, interval values, subgroup sample counts and original-vs-repeat-1 provenance. Read any warnings before using the outputs. Plotting code was not changed during packaging. Outdated claims that PCA plus covariates was unevaluated and outdated placement-size instructions were corrected in markdown.

## Poster PDFs

[Supplied poster PDF](../poster/Rashrash_Michigan_AI_Symposium_2026_Poster.pdf): original user-supplied bytes; one 11 x 8.5-inch page with margins. This is the primary online viewing copy.

[40 x 30-inch export](../poster/Rashrash_Poster_40x30_Export.pdf): the earlier export from the supplied tenth-draft PowerPoint. This is a separate file and must not be described as the exact printer-submitted PDF. It was not resized from the letter-size copy.
