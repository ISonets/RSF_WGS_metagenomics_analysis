# RSF_WGS_metagenomics_analysis
Analysis of RSF WGS metagenomics data from hospitals in 2 timepotins: code, plots, some data

**Rmds**:
  - *RSF_permdisp_check*: check for PERMDISP across all covariates in metadata to check if centroid differences are **not** explained by dispersion differences;
  - *alpha_div_timepoints*: alpha-diversity analysis using different indices (Shannon, Chao1, Simpson (the last one works somewhat unstable though)) between 3 groups and 2 timepoints;
  - *beta_div* : beta-diversity analysis using weghted Unifrac, Jaccard and Bray-Curtis distances mertics and ANOSIM test for 3 groups and 2 timepoints;
  - *bray-curtis_boxplot*: pariwise Bray-Curtis distance calculation between 2 timepoints of each sample while grouping by covariates from metadata;
  - *chi-square*: check if distirbution of covariates from metadata are linked with Group distibution;
  - *create_phyloseqs*: code for phyloseq creation for WGS/HUMAnN/MAGs datasets. also some debugginf in case something goes wrong with sample names and other stuff to ensure we didn't lost any of samples;
  - *deseq_type3_analysis*: DESeq2 analysis using poscounts, Wald test, local fit type, fitTypeBH adjustment, logFC shrinkage for WGS dataset(also can be easily adjusted for MAG analysis due to phyloseq standard configuration);
  - *enterotypes*: enterotype analysis with logging using PAM and checking silhoette score and also some other rare metrics. DMM failed and stuck, so have to omit it;
  - *heatmaps_RSF*: just some heatmaps with some clustering(eulcidean distances and Ward.D2(D2 means sum of squared errors) method);
  - *maaslin2_humann_RSF*: MaAsLin2 analysis for HUMAnN predicted metabolic pathways, includes LM and NEGBIN models, compositional data transformation or no transformation, CSS and TMM normalizations. also some debugs and previous legacy version sof analysis are included to ease of tracking changes;
  - *metadata_distribution*: just some metadata plot for article, nothing fancy;
  - *permanova_new_plot*: custom plot for PERMANOVA analysis, uses VIF check and by=margin (3rd type of SqS, to ensure covariates' order in formula are not significant) and R2adjusted;
  - *top_taxa*: just top-15 families in WGS taxonomy grouped by Timepoint and Group.
