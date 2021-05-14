# Comparative analyses of bite-force among lepidosaurs

Author(s): Justin E Isip, Marc EH Jones and [Natalie Cooper](mailto:natalie.cooper.@nhm.ac.uk).

This repository contains all the code and some data used in the [paper](add link later). 

![alt text](https://github.com/nhcooper123/lepidosaur-biteforce/raw/main/figures/phylogeny-data-coverage-colours.png)

To cite the paper: 
> Justin E Isip, Marc EH Jones and Natalie Cooper. Comparative analyses of bite-force among lepidosaurs.

To cite this repo: 
> Justin E Isip, Marc EH Jones and Natalie Cooper. 2021. GitHub: nhcooper123/lepidosaur-biteforce. Zenodo. DOI: [add doi on acceptance].

[![DOI](https://zenodo.org/badge/161480153.svg)](https://zenodo.org/badge/latestdoi/161480153) [add doi badge]

## Data

* `/data` contains the cleaned data used in the analyses, including the phylogeny.

Raw data are not included in this repo due to size limitations. All raw and cleaned data are available from the [NHM Data Portal](https://doi.org/10.5519/dkrhpxjh). 

If you use the cleaned data please cite as follows: 
> Justin E Isip, Marc EH Jones and Natalie Cooper (2021). Dataset: Lepidosaur bite-force data. Natural History Museum Data Portal (data.nhm.ac.uk). https://doi.org/10.5519/dkrhpxjh.

**Please cite the original sources of the data as follows where possible.**

The ecological data are all from Meiri et al (2018). Please cite this paper if you use these data!

Meiri, S. Traits of lizards of the world: Variation around a successful evolutionary design. Global Ecol Biogeogr. 2018; 27: 1168– 1172. https://doi.org/10.1111/geb.12773

The phylogeny comes from Wright et al (2015). Please cite this paper if you use these data!

Wright, AM, Lyons, KM, Brandley, MC, Hillis, DM. 2015. Which came first: the lizard or the egg? Robustness in phylogenetic reconstruction of ancestral states. J. Exp. Zool. (Mol. Dev. Evol.) 324B: 504– 516.



-------
## Analyses
The analysis code is divided into `.Rmd` files that run the analyses for each section of the paper/supplementary materials, and more detailed scripts for the figures found in the paper.

Note that throughout I've commented out `ggsave` commands so you don't clog your machine up with excess plots you don't need.

1. **01-wrangle-data.Rmd** wrangles the raw data into a useable format.
2. **01B-wrangle-phylogeny.Rmd** wrangles the phylogeny into a useable format.
3. **01C-family-phylogeny.Rmd** builds a family level phylogeny.
4. **02A-data-taxonomy-phylogeny.Rmd**
5. **02B-data-bite-force.Rmd** 
6. **02C-data-bite-force-meansd.Rmd**
7. **03A-analyses-mean.Rmd** runs all analyses on maximum bite-force data across all species.
8. **03B-analyses-mean-sd.Rmd** runs all analyses on maximum bite-force data plus SD across all species.
9. **03C-analyses-mean-basictree.Rmd** runs all analyses on maximum bite-force data across all species minus the species added to the phylogeny.
10. **03D-analyses-mean-sd-basictree.Rmd** runs all analyses on maximum bite-force plus SD data across all species minus the species added to the phylogeny.
11. **03E-species-in-each-analysis.Rmd** outputs the numbers of species involved in each analysis.
12. **04A-bodysize-mean.Rmd**
13. **04B-bodysize-mean-sd.Rmd**
14. **04C-bodysize-mean-basictree.Rmd**
15. **04D-bodysize-mean-sd-basictree.Rmd**
16. **05-bodysize-figures.Rmd** creates figures for body size versus bite-force plots.
17. **06-ecology-figures.Rmd** creates figures for body size versus bite-force coloured by diet or habit plots.
18. **07-acrodont-figures.Rmd** creates figures for body size versus bite-force coloured by tooth attachment plots.


-------
## Other folders

* `/figures` contains the figures
* `/tablees` contains the statistical results for tables
* `/manuscript` contains the LaTeX files for the paper

-------
## Session Info


## Checkpoint for reproducibility
To rerun all the code with packages as they existed on CRAN at time of our analyses we recommend using the `checkpoint` package, and running this code prior to the analysis:

```{r}
checkpoint("2021-14-05")
```
