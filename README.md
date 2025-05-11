# SURV675_HW3

## Background Information
This Project used data from GESIS. The goal of the assignment was to use real-world data to create an analytic notebook looking at the change in time in the number of COVID cases. This involved the following:

1. Create a local Spark server and add data 
  You can access the datasets about COVID-19 from this GitHub repository: [CSSEGISandData](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data) The two files that were used for this project were the [confirmed global time series data](https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv), and the [UID Lookup Table](https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/UID_ISO_FIPS_LookUp_Table.csv).
2. Merge the two datasets, make a smaller version that only includes a few countries, then calculate the number of cases and rate of cases by country and day. Graph the results and interpret. 
3. Run a linear regression explaining the log of the number of cases and interpret the results. 
4. Ensure the pdf Markdown file shows all syntax used, the results, and walk the reader through the steps of the analysis. 
5. Ensure clean presentation of the report, Github repo, and the rest. 


## Below is the information needed for reproducability: Session Info
R version 4.4.1 (2024-06-14 ucrt)
Platform: x86_64-w64-mingw32/x64
Running under: Windows 11 x64 (build 26100)

Matrix products: default


locale:
[1] LC_COLLATE=English_United States.utf8  LC_CTYPE=English_United States.utf8    LC_MONETARY=English_United States.utf8
[4] LC_NUMERIC=C                           LC_TIME=English_United States.utf8    

time zone: America/New_York
tzcode source: internal

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] corrr_0.4.4     dbplot_0.3.3    DBI_1.2.3       haven_2.5.4     lubridate_1.9.3 forcats_1.0.0   stringr_1.5.1   dplyr_1.1.4     purrr_1.0.2    
[10] readr_2.1.5     tidyr_1.3.1     tibble_3.2.1    ggplot2_3.5.1   tidyverse_2.0.0 sparklyr_1.9.0 

loaded via a namespace (and not attached):
 [1] gtable_0.3.6      xfun_0.48         lattice_0.22-6    tzdb_0.4.0        vctrs_0.6.5       tools_4.4.1       generics_0.1.3    parallel_4.4.1   
 [9] blob_1.2.4        pkgconfig_2.0.3   Matrix_1.7-2      dbplyr_2.5.0      uuid_1.2-1        lifecycle_1.0.4   compiler_4.4.1    farver_2.1.2     
[17] munsell_0.5.1     htmltools_0.5.8.1 yaml_2.3.10       pillar_1.10.1     crayon_1.5.3      openssl_2.3.2     nlme_3.1-167      tidyselect_1.2.1 
[25] digest_0.6.37     stringi_1.8.4     labeling_0.4.3    splines_4.4.1     fastmap_1.2.0     grid_4.4.1        colorspace_2.1-1  cli_3.6.3        
[33] magrittr_2.0.3    utf8_1.2.4        withr_3.0.2       scales_1.3.0      bit64_4.6.0-1     timechange_0.3.0  rmarkdown_2.29    httr_1.4.7       
[41] config_0.3.2      bit_4.5.0.1       askpass_1.2.1     hms_1.1.3         evaluate_1.0.3    knitr_1.49        mgcv_1.9-1        rlang_1.1.4      
[49] glue_1.8.0        pkgload_1.4.0     rstudioapi_0.17.1 vroom_1.6.5       jsonlite_1.9.1    R6_2.6.1    
