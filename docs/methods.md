# Methods

Both cohorts use ln(TPM + 1) expression aligned to the model vocabulary. PCA is fitted within training folds to retain 90% of variance. Frozen BulkFormer-37M embeddings comprise 128 learned dimensions and three expression summaries. Both feed ridge logistic regression with balanced class weights.

Pooled analyses use five outer folds, four inner folds, and five seeds (20260921–20260925). Inner CV selects C from 0.001, 0.01, 0.1, 1, 10, and 100. Preprocessing is fitted within training folds. Pooled out-of-fold AUROC is calculated separately for each repeat, then averaged. Mean fold AUROC is reported as a sensitivity analysis.

The paired bootstrap uses 5,000 class-stratified resamples of fixed original predictions. Separate-sex models use four outer and three inner folds for one partition. Pooled-model subgroup evaluation is a different analysis. Sex comparisons are exploratory and unadjusted for multiplicity.

Feature ablation compares all 131 dimensions, the 128 learned dimensions, and three summaries. Removing appended summaries does not remove any contribution of summaries within the pretrained encoder. Covariate comparisons include age, BMI, and sex alone and appended to each representation. Extended MDD covariates are explicitly labelled as a reconstructed specification.

Mixed-cohort age/sex matching pairs each control with the nearest-age case of the same sex without replacement. It has no caliper and depends on matching order. Existing held-out predictions are rescored without refitting.
