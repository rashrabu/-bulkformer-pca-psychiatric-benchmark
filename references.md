# References

## Papers cited on the poster

1. Kang, B., Fan, R., Yi, M., Cui, C., & Cui, Q. (2026). **BulkFormer: A large-scale foundation model for bulk transcriptomes.** *Cell Systems*, article 101657. https://doi.org/10.1016/j.cels.2026.101657
   - Official implementation: https://github.com/KangBoming/BulkFormer
   - Benchmark source commit: `5bcf5b99e799cd55f41e4d6fe8200b2cdf3d9589`.
   - This benchmark uses the saved 37M checkpoint embeddings, not every model configuration described in the paper or current repository.

2. Amazigh Mokhtari, El Chérif Ibrahim, Arnaud Gloaguen, Claire-Cécile Barrot, David Cohen, Margot Derouin, Hortense Vachon, Guillaume Charbonnier, Béatrice Loriod, Charles Decraene, Ipek Yalcin, Cynthia Marie-Claire, Bruno Etain, Raoul Belzeaux, Andrée Delahaye-Duriez, Pierre-Eric Lutz (2025). **Using multiomic integration to improve blood biomarkers of major depressive disorder: a case-control study.** *EBioMedicine, 113*, 105569. https://doi.org/10.1016/j.ebiom.2025.105569
   - Cohort: GSE251778.
   - Author code: https://github.com/INSERM-U1141-Neurodiderot/multiomics_MDD

3. Ghalia Rehawi, Jonas Hagenberg, Philipp G. Sämann, Lambert Moyon, Elisabeth Binder, Markus List, Annalisa Marsico, Janine Knauer-Arloth; BeCOME study group; OPTIMA study group (2025). **Integrative gene and isoform co-expression networks reveal regulatory rewiring in stress-related psychiatric disorders.** *iScience, 28*(9), 113342. https://doi.org/10.1016/j.isci.2025.113342
   - Cohort: GSE289146. The benchmark uses a broader psychiatric case group, not an MDD-only cohort.

4. Osimo, E. F., Baxter, L. J., Lewis, G., Jones, P. B., & Khandaker, G. M. (2019). **Prevalence of low-grade inflammation in depression: a systematic review and meta-analysis of CRP levels.** *Psychological Medicine, 49*(12), 1958–1970. https://doi.org/10.1017/S0033291719001454
   - Background reference for inflammation; the benchmark does not directly test CRP or inflammatory causation.

## Data records

- GSE251778: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE251778
- GSE289146: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE289146

## Software and preprocessing documentation

- RSEM output definitions: https://deweylab.github.io/RSEM/rsem-calculate-expression.html
- scikit-learn: https://scikit-learn.org/stable/
- BioRender (poster illustration): https://www.biorender.com/

Package versions and source commits are recorded by the notebook's analysis manifest. The cohort publications describe their original studies; preprocessing and evaluation choices specific to this benchmark are documented in the notebook.
