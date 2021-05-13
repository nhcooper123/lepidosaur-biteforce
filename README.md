# comparative analyses of bite-force among lepidosuars

![alt text](https://github.com/nhcooper123/lepidosaur-biteforce/raw/master/manuscript/figures/phylogeny-data-coverage-colours.png)


Author(s): Justin E Isip, Marc EH Jones and [Natalie Cooper](mailto:natalie.cooper.@nhm.ac.uk).

This repository contains all the code and some data used in the [paper](add link later). 

To cite the paper: 
> Justin E Isip, Marc EH Jones and Natalie Cooper. Comparative analyses of bite-force among lepidosaurs.

To cite this repo: 
> Justin E Isip, Marc EH Jones and Natalie Cooper. 2021. GitHub: nhcooper123/lepidosaur-biteforce. Zenodo. DOI: [add doi on acceptance].

[![DOI](https://zenodo.org/badge/161480153.svg)](https://zenodo.org/badge/latestdoi/161480153) [add doi badge]

## Data
All cleaned data are available from the [NHM Data Portal](ADD LINK).

If you use the cleaned data please cite as follows: 
> Justin E Isip, Marc EH Jones and Natalie Cooper (2021). Dataset: Lepidosaur bite force data. Natural History Museum Data Portal (data.nhm.ac.uk). ADD LINK.

Please cite the original sources of the data as follows where possible.

-------
## Analyses
The analysis code is divided into `.Rmd` files that run the analyses for each section of the paper/supplementary materials, and more detailed scripts for the figures found in the paper.

Note that throughout I've commented out `ggsave` commands so you don't clog your machine up with excess plots you don't need.

1. **xxx.Rmd** wrangles the specimen data into a useable format.


-------
## Other folders

* `/figures` contains the figures
* `/manuscript` contains the LaTeX files for the paper

-------
## Session Info


## Checkpoint for reproducibility
To rerun all the code with packages as they existed on CRAN at time of our analyses we recommend using the `checkpoint` package, and running this code prior to the analysis:

```{r}
checkpoint("2020-11-06")
```
