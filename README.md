# RNAseq-Source-Code
The RNAseq Analysis Source Code

#### Package Versions and R sessionInfo
```
R version 3.4.4 (2018-03-15)
Platform: x86_64-pc-linux-gnu (64-bit)
Running under: Ubuntu 14.04.6 LTS

Matrix products: default
BLAS: /usr/lib/atlas-base/atlas/libblas.so.3.0
LAPACK: /usr/lib/lapack/liblapack.so.3.0

locale:
 [1] LC_CTYPE=en_US.UTF-8       LC_NUMERIC=C              
 [3] LC_TIME=en_US.UTF-8        LC_COLLATE=en_US.UTF-8    
 [5] LC_MONETARY=zh_CN.UTF-8    LC_MESSAGES=en_US.UTF-8   
 [7] LC_PAPER=zh_CN.UTF-8       LC_NAME=C                 
 [9] LC_ADDRESS=C               LC_TELEPHONE=C            
[11] LC_MEASUREMENT=zh_CN.UTF-8 LC_IDENTIFICATION=C       

attached base packages:
 [1] grid      stats4    parallel  stats     graphics  grDevices utils    
 [8] datasets  methods   base     

other attached packages:
 [1] survminer_0.4.6            ggpubr_0.2.4              
 [3] magrittr_1.5               survival_3.1-8            
 [5] BiocParallel_1.12.0        WGCNA_1.68                
 [7] fastcluster_1.1.25         dynamicTreeCut_1.63-1     
 [9] dendextend_1.13.2          VennDiagram_1.6.20        
[11] futile.logger_1.4.3        pheatmap_1.0.12           
[13] ReactomePA_1.22.0          DOSE_3.4.0                
[15] stringr_1.4.0              ggplot2_3.3.2             
[17] edgeR_3.20.9               limma_3.34.9              
[19] DESeq2_1.18.1              SummarizedExperiment_1.8.1
[21] DelayedArray_0.4.1         matrixStats_0.56.0        
[23] ensembldb_2.2.2            AnnotationFilter_1.2.0    
[25] GenomicFeatures_1.30.3     AnnotationDbi_1.40.0      
[27] Biobase_2.38.0             GenomicRanges_1.30.3      
[29] GenomeInfoDb_1.14.0        IRanges_2.12.0            
[31] S4Vectors_0.16.0           AnnotationHub_2.10.1      
[33] BiocGenerics_0.24.0       

loaded via a namespace (and not attached):
  [1] backports_1.1.8               Hmisc_4.3-0                  
  [3] fastmatch_1.1-0               plyr_1.8.5                   
  [5] igraph_1.2.4.2                lazyeval_0.2.2               
  [7] splines_3.4.4                 robust_0.4-18.1              
  [9] digest_0.6.25                 foreach_1.4.7                
 [11] BiocInstaller_1.28.0          htmltools_0.4.0              
 [13] GOSemSim_2.4.1                viridis_0.5.1                
 [15] GO.db_3.5.0                   checkmate_1.9.4              
 [17] memoise_1.1.0                 fit.models_0.5-14            
 [19] doParallel_1.0.15             cluster_2.1.0                
 [21] Biostrings_2.46.0             annotate_1.56.2              
 [23] prettyunits_1.1.1             colorspace_1.4-1             
 [25] rrcov_1.4-7                   blob_1.2.0                   
 [27] rappdirs_0.3.1                xfun_0.11                    
 [29] dplyr_1.0.0                   crayon_1.3.4                 
 [31] RCurl_1.98-1.2                graph_1.56.0                 
 [33] genefilter_1.60.0             impute_1.52.0                
 [35] zoo_1.8-6                     iterators_1.0.12             
 [37] glue_1.4.1                    gtable_0.3.0                 
 [39] zlibbioc_1.24.0               XVector_0.18.0               
 [41] graphite_1.24.1               DEoptimR_1.0-8               
 [43] scales_1.1.1                  mvtnorm_1.0-7                
 [45] futile.options_1.0.1          DBI_1.1.0                    
 [47] Rcpp_1.0.5                    viridisLite_0.3.0            
 [49] xtable_1.8-4                  progress_1.2.2               
 [51] htmlTable_1.13.3              foreign_0.8-72               
 [53] bit_1.1-14                    reactome.db_1.62.0           
 [55] km.ci_0.5-2                   preprocessCore_1.40.0        
 [57] Formula_1.2-3                 htmlwidgets_1.5.1            
 [59] httr_1.4.1                    fgsea_1.4.1                  
 [61] RColorBrewer_1.1-2            acepack_1.4.1                
 [63] ellipsis_0.3.1                pkgconfig_2.0.3              
 [65] XML_3.98-1.20                 nnet_7.3-12                  
 [67] locfit_1.5-9.1                tidyselect_1.1.0             
 [69] rlang_0.4.7                   reshape2_1.4.3               
 [71] later_1.0.0                   munsell_0.5.0                
 [73] tools_3.4.4                   generics_0.0.2               
 [75] RSQLite_2.1.5                 broom_0.5.2                  
 [77] fastmap_1.0.1                 yaml_2.2.0                   
 [79] knitr_1.26                    bit64_0.9-7                  
 [81] robustbase_0.93-5             survMisc_0.5.5               
 [83] purrr_0.3.4                   nlme_3.1-142                 
 [85] mime_0.8                      formatR_1.7                  
 [87] DO.db_2.9                     biomaRt_2.34.2               
 [89] compiler_3.4.4                rstudioapi_0.11              
 [91] curl_4.3                      interactiveDisplayBase_1.16.0
 [93] ggsignif_0.6.0                tibble_3.0.3                 
 [95] geneplotter_1.56.0            pcaPP_1.9-73                 
 [97] stringi_1.4.6                 lattice_0.20-38              
 [99] ProtGenerics_1.10.0           Matrix_1.2-18                
[101] KMsurv_0.1-5                  vctrs_0.3.1                  
[103] pillar_1.4.6                  lifecycle_0.2.0              
[105] BiocManager_1.30.10           data.table_1.12.8            
[107] bitops_1.0-6                  httpuv_1.5.2                 
[109] rtracklayer_1.38.3            qvalue_2.10.0                
[111] R6_2.4.1                      latticeExtra_0.6-28          
[113] RMySQL_0.10.17                promises_1.1.0               
[115] gridExtra_2.3                 codetools_0.2-16             
[117] lambda.r_1.2.4                MASS_7.3-51.4                
[119] withr_2.2.0                   GenomicAlignments_1.14.2     
[121] Rsamtools_1.30.0              GenomeInfoDbData_1.0.0       
[123] hms_0.5.2                     rpart_4.1-15                 
[125] tidyr_1.1.0                   rvcheck_0.1.7                
[127] shiny_1.4.0                   base64enc_0.1-3
```

#### Instructions for Use 

Please modify the download count data from Gene Expression Omnibus and change the path in jupyter notebook, then run the code within R

#### Reproducibility
The expected output was descripted in our article method section, and the output figure labels and colors could be further modified by Adobe Illustrator
