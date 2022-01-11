# Comparative analyses of bite-force among lepidosaurs

Author(s): Justin E Isip, Marc EH Jones and [Natalie Cooper](mailto:natalie.cooper.@nhm.ac.uk).

This repository contains all the code and some data used in the [paper](http://dx.doi.org/10.1098/rspb.2021.2493). 

![alt text](https://github.com/nhcooper123/lepidosaur-biteforce/raw/main/figures/phylogeny-data-coverage-colours.png)

To cite the paper: 
> Justin E Isip, Marc EH Jones and Natalie Cooper. 2022. Clade-wide variation in bite-force performance is determined primarily by size not ecology. Proceedings of the Royal Society B: Biological Sciences. DOI: 10.1098/rspb.2021.2493.

To cite this repo: 
> Justin E Isip, Marc EH Jones and Natalie Cooper. 2021. GitHub: nhcooper123/lepidosaur-biteforce. Zenodo. 

## Data

* `/data` contains the cleaned data used in the analyses, including the phylogeny.

Raw data are not included in this repo due to size limitations. All raw and cleaned data are available from the [NHM Data Portal](https://doi.org/10.5519/dkrhpxjh). 

If you use the cleaned data please cite as follows: 
> Justin E Isip, Marc EH Jones and Natalie Cooper (2021). Dataset: Lepidosaur bite-force data. Natural History Museum Data Portal (data.nhm.ac.uk). https://doi.org/10.5519/dkrhpxjh.

**Please cite the original sources of the data where possible.**

The ecological data are all from Meiri et al (2018). **Please cite this paper if you use these data!**

Meiri, S. Traits of lizards of the world: Variation around a successful evolutionary design. Global Ecol Biogeogr. 2018; 27: 1168– 1172. https://doi.org/10.1111/geb.12773

The phylogeny comes from Wright et al (2015). **Please cite this paper if you use these data!**

Wright, AM, Lyons, KM, Brandley, MC, Hillis, DM. 2015. Which came first: the lizard or the egg? Robustness in phylogenetic reconstruction of ancestral states. J. Exp. Zool. (Mol. Dev. Evol.) 324B: 504– 516.

-------
## Analyses
The analysis code is divided into `.Rmd` files that run the analyses for each section of the paper/supplementary materials, and more detailed scripts for the figures found in the paper.

Note that throughout I've commented out `ggsave` commands so you don't clog your machine up with excess plots you don't need.

1. **01-wrangle-data.Rmd** wrangles the raw data into a useable format.
2. **01B-wrangle-phylogeny.Rmd** wrangles the phylogeny into a useable format.
3. **01C-family-phylogeny.Rmd** builds a family level phylogeny.
4. **02A-data-taxonomy-phylogeny.Rmd** explores bite-force variation across taxonomic groups and phylogeny. Creates Figures 1 and S1.
5. **02B-data-bite-force.Rmd** explores distributions of bite-force and other data across taxonomic and ecological groups. Creats Figures S2, S3 and S4.
6. **02C-data-bite-force-meansd.Rmd** explores distributions of bite-force plus SD across taxonomic and ecological groups.
7. **03A-analyses-mean.Rmd** runs all analyses on maximum bite-force as a function of size (SVL, or head measures) and various ecological factors or taxonomic groupings across all species and both sexes combined and separately. These are the main analyses for the paper.
8. **03B-analyses-mean-sd.Rmd** same as 3A but using maximum bite-force data plus SD.
9. **03C-analyses-mean-basictree.Rmd** same as 3A minus the species added to the original phylogeny.
10. **03D-analyses-mean-sd-basictree.Rmd** same as 3B minus the species added to the original phylogeny.
11. **03E-species-in-each-analysis.Rmd** outputs the numbers of species involved in each analysis in 3A-3D.
20. **03F-acrodont-sensitivity-analyses.Rmd** repeats the analyses in 3A for a different definition of acrodonty to ensure the results are robust.
12. **04A-bodysize-mean.Rmd** runs all analyses on maximum bite-force as a function of size only (SVL, or head measures) across all species and both sexes combined and separately. 
13. **04B-bodysize-mean-sd.Rmd** same as 4A but using maximum bite-force data plus SD.
14. **04C-bodysize-mean-basictree.Rmd** same as 4A minus the species added to the original phylogeny.
15. **04D-bodysize-mean-sd-basictree.Rmd** same as 4B minus the species added to the original phylogeny.
16. **05-bodysize-figures.Rmd** creates figures for body size versus bite-force plots, including Figure 2.
17. **06-ecology-figures.Rmd** creates figures for body size versus bite-force coloured by diet or habit plots, including Figures 3, 4, S5, S7 and S8.
18. **07-diet-distribution-figures.Rmd** creates Figure S6, showing how SVL and bite-force vary across diet categories.

-------
## Other folders

* `/figures` contains the figures
* `/outputs` contains the statistical results for tables

-------
## Session Info
For reproducibility purposes, here is the output of `devtools::session_info()` used to perform the analyses in the publication.

    ─ Session info ────────────────────────────────────────────────────────────────────────────────────
    setting  value                       
    version  R version 4.0.3 (2020-10-10)
    os       macOS Catalina 10.15.7      
    system   x86_64, darwin17.0          
    ui       RStudio                     
    language (EN)                        
    collate  en_GB.UTF-8                 
    ctype    en_GB.UTF-8                 
    tz       Europe/London               
    date     2022-01-11                  

    ─ Packages ────────────────────────────────────────────────────────────────────────────────────────
    package           * version    date       lib source        
    ape               * 5.5        2021-04-25 [1] CRAN (R 4.0.2)
    aplot               0.0.6      2020-09-03 [1] CRAN (R 4.0.3)
    assertthat          0.2.1      2019-03-21 [1] CRAN (R 4.0.2)
    backports           1.2.1      2020-12-09 [1] CRAN (R 4.0.2)
    BiocManager         1.30.10    2019-11-16 [1] CRAN (R 4.0.2)
    broom             * 0.7.5      2021-02-19 [1] CRAN (R 4.0.2)
    cachem              1.0.4      2021-02-13 [1] CRAN (R 4.0.2)
    callr               3.5.1      2020-10-13 [1] CRAN (R 4.0.2)
    caper             * 1.0.1      2018-04-17 [1] CRAN (R 4.0.2)
    cellranger          1.1.0      2016-07-27 [1] CRAN (R 4.0.2)
    cli                 2.3.1      2021-02-23 [1] CRAN (R 4.0.2)
    clusterGeneration   1.3.7      2020-12-15 [1] CRAN (R 4.0.2)
    coda                0.19-4     2020-09-30 [1] CRAN (R 4.0.2)
    colorspace          2.0-0      2020-11-11 [1] CRAN (R 4.0.3)
    combinat            0.0-8      2012-10-29 [1] CRAN (R 4.0.2)
    crayon              1.4.1      2021-02-08 [1] CRAN (R 4.0.2)
    DBI                 1.1.1      2021-01-15 [1] CRAN (R 4.0.2)
    dbplyr              2.1.0      2021-02-03 [1] CRAN (R 4.0.2)
    desc                1.3.0      2021-03-05 [1] CRAN (R 4.0.2)
    deSolve             1.28       2020-03-08 [1] CRAN (R 4.0.2)
    devtools            2.3.2      2020-09-18 [1] CRAN (R 4.0.2)
    digest              0.6.27     2020-10-24 [1] CRAN (R 4.0.2)
    dplyr             * 1.0.5      2021-03-05 [1] CRAN (R 4.0.2)
    ellipsis            0.3.1      2020-05-15 [1] CRAN (R 4.0.2)
    evaluate            0.14       2019-05-28 [1] CRAN (R 4.0.1)
    expm                0.999-6    2021-01-13 [1] CRAN (R 4.0.2)
    fansi               0.4.2      2021-01-15 [1] CRAN (R 4.0.2)
    fastmap             1.1.0      2021-01-25 [1] CRAN (R 4.0.2)
    fastmatch           1.1-0      2017-01-28 [1] CRAN (R 4.0.2)
    forcats           * 0.5.1      2021-01-27 [1] CRAN (R 4.0.2)
    fs                  1.5.0      2020-07-31 [1] CRAN (R 4.0.2)
    geiger            * 2.0.7      2020-06-02 [1] CRAN (R 4.0.2)
    generics            0.1.0      2020-10-31 [1] CRAN (R 4.0.2)
    ggplot2           * 3.3.3      2020-12-30 [1] CRAN (R 4.0.2)
    ggstance          * 0.3.5      2020-12-17 [1] CRAN (R 4.0.2)
    ggtree            * 2.4.1      2020-11-13 [1] Bioconductor  
    glue                1.4.2      2020-08-27 [1] CRAN (R 4.0.2)
    gtable              0.3.0      2019-03-25 [1] CRAN (R 4.0.2)
    gtools              3.8.2      2020-03-31 [1] CRAN (R 4.0.2)
    haven               2.3.1      2020-06-01 [1] CRAN (R 4.0.2)
    here              * 1.0.1      2020-12-13 [1] CRAN (R 4.0.2)
    hms                 1.0.0      2021-01-13 [1] CRAN (R 4.0.2)
    htmltools           0.5.1.1    2021-01-22 [1] CRAN (R 4.0.2)
    httr                1.4.2      2020-07-20 [1] CRAN (R 4.0.2)
    igraph              1.2.6      2020-10-06 [1] CRAN (R 4.0.2)
    jsonlite            1.7.2      2020-12-09 [1] CRAN (R 4.0.2)
    knitr             * 1.31       2021-01-27 [1] CRAN (R 4.0.2)
    lattice             0.20-41    2020-04-02 [1] CRAN (R 4.0.3)
    lazyeval            0.2.2      2019-03-15 [1] CRAN (R 4.0.2)
    lifecycle           1.0.0      2021-02-15 [1] CRAN (R 4.0.2)
    lubridate           1.7.10     2021-02-26 [1] CRAN (R 4.0.2)
    magrittr            2.0.1      2020-11-17 [1] CRAN (R 4.0.2)
    maps              * 3.3.0      2018-04-03 [1] CRAN (R 4.0.2)
    MASS              * 7.3-53.1   2021-02-12 [1] CRAN (R 4.0.2)
    Matrix              1.3-2      2021-01-06 [1] CRAN (R 4.0.2)
    memoise             2.0.0      2021-01-26 [1] CRAN (R 4.0.2)
    mnormt              2.0.2      2020-09-01 [1] CRAN (R 4.0.2)
    modelr              0.1.8      2020-05-19 [1] CRAN (R 4.0.2)
    munsell             0.5.0      2018-06-12 [1] CRAN (R 4.0.2)
    mvtnorm           * 1.1-1      2020-06-09 [1] CRAN (R 4.0.2)
    nlme                3.1-152    2021-02-04 [1] CRAN (R 4.0.2)
    numDeriv            2016.8-1.1 2019-06-06 [1] CRAN (R 4.0.2)
    patchwork         * 1.1.1      2020-12-17 [1] CRAN (R 4.0.2)
    phangorn            2.5.5      2019-06-19 [1] CRAN (R 4.0.2)
    phytools          * 0.7-70     2020-09-19 [1] CRAN (R 4.0.2)
    pillar              1.5.1      2021-03-05 [1] CRAN (R 4.0.2)
    pkgbuild            1.2.0      2020-12-15 [1] CRAN (R 4.0.2)
    pkgconfig           2.0.3      2019-09-22 [1] CRAN (R 4.0.2)
    pkgload             1.2.0      2021-02-23 [1] CRAN (R 4.0.2)
    plotrix             3.8-1      2021-01-21 [1] CRAN (R 4.0.2)
    prettyunits         1.1.1      2020-01-24 [1] CRAN (R 4.0.2)
    processx            3.4.5      2020-11-30 [1] CRAN (R 4.0.2)
    ps                  1.6.0      2021-02-28 [1] CRAN (R 4.0.2)
    purrr             * 0.3.4      2020-04-17 [1] CRAN (R 4.0.2)
    quadprog            1.5-8      2019-11-20 [1] CRAN (R 4.0.2)
    R6                  2.5.0      2020-10-28 [1] CRAN (R 4.0.2)
    Rcpp                1.0.7      2021-07-07 [1] CRAN (R 4.0.2)
    readr             * 1.4.0      2020-10-05 [1] CRAN (R 4.0.2)
    readxl              1.3.1      2019-03-13 [1] CRAN (R 4.0.2)
    remotes             2.2.0      2020-07-21 [1] CRAN (R 4.0.2)
    reprex              1.0.0      2021-01-27 [1] CRAN (R 4.0.2)
    rlang               0.4.10     2020-12-30 [1] CRAN (R 4.0.2)
    rmarkdown           2.7        2021-02-19 [1] CRAN (R 4.0.2)
    rprojroot           2.0.2      2020-11-15 [1] CRAN (R 4.0.2)
    rstudioapi          0.13       2020-11-12 [1] CRAN (R 4.0.2)
    rvcheck             0.1.8      2020-03-01 [1] CRAN (R 4.0.2)
    rvest               1.0.0      2021-03-09 [1] CRAN (R 4.0.2)
    scales              1.1.1      2020-05-11 [1] CRAN (R 4.0.2)
    scatterplot3d       0.3-41     2018-03-14 [1] CRAN (R 4.0.2)
    sessioninfo         1.1.1      2018-11-05 [1] CRAN (R 4.0.2)
    stringi             1.5.3      2020-09-09 [1] CRAN (R 4.0.2)
    stringr           * 1.4.0      2019-02-10 [1] CRAN (R 4.0.2)
    subplex             1.6        2020-02-23 [1] CRAN (R 4.0.2)
    testthat            3.0.2      2021-02-14 [1] CRAN (R 4.0.2)
    tibble            * 3.1.0      2021-02-25 [1] CRAN (R 4.0.2)
    tidyr             * 1.1.3      2021-03-03 [1] CRAN (R 4.0.2)
    tidyselect          1.1.0      2020-05-11 [1] CRAN (R 4.0.2)
    tidytree          * 0.3.3      2020-04-02 [1] CRAN (R 4.0.2)
    tidyverse         * 1.3.0      2019-11-21 [1] CRAN (R 4.0.2)
    tmvnsim             1.0-2      2016-12-15 [1] CRAN (R 4.0.2)
    treeio            * 1.14.3     2020-11-19 [1] Bioconductor  
    usethis             2.0.1      2021-02-10 [1] CRAN (R 4.0.2)
    utf8                1.1.4      2018-05-24 [1] CRAN (R 4.0.2)
    vctrs               0.3.6      2020-12-17 [1] CRAN (R 4.0.2)
    withr               2.4.1      2021-01-26 [1] CRAN (R 4.0.2)
    xfun                0.22       2021-03-11 [1] CRAN (R 4.0.3)
    xml2                1.3.2      2020-04-23 [1] CRAN (R 4.0.2)
    yaml                2.2.1      2020-02-01 [1] CRAN (R 4.0.2)

    [1] /Library/Frameworks/R.framework/Versions/4.0/Resources/library

## Checkpoint for reproducibility
To rerun all the code with packages as they existed on CRAN at time of our analyses we recommend using the `checkpoint` package, and running this code prior to the analysis:

```{r}
checkpoint("2021-14-05")
```
