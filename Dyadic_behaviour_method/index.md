## Supplementary material for the paper: <br />
## A relative-motion method for parsing spatio-temporal behaviour of dyads using GPS relocation data <br />

Authors: [Ludovica Luisa Vissat](https://ourenvironment.berkeley.edu/people/ludovica-luisa-vissat), [Jason K. Blackburn](https://geog.ufl.edu/faculty/blackburn/), [Wayne M. Getz](https://ourenvironment.berkeley.edu/people/wayne-marcus-getz) <br />
l.luisavissat@berkeley.edu, jkblackburn@ufl.edu, wgetz@berkeley.edu

### Numerus Model Builder (NMB) models <br />

To generate the data used in Section 3, we defined and simulated the following NMB models, explained in details in our [SOF](https://ludovicalv.github.io/PDFs/Elep_paper.pdf). 

- The distance-dependent behaviour model (Model_distance.nmb) can be downloaded [here](http://doi.org/10.5281/zenodo.4961965).

- The time-dependent behaviour model (Model_time.nmb) can be downloaded [here](http://doi.org/10.5281/zenodo.4961965).

Visit [numerusinc.com](https://www.numerusinc.com/) to download the latest version of NMB.

### Simulated data: NMB output <br />

- The output of a simulation of the distance-dependent behaviour model can be downloaded [here](http://doi.org/10.5281/zenodo.4961965) for both individual A (ModelDistance_A.csv) and B (ModelDistance_B.csv).

- The output of a simulation of the time-dependent behaviour model can be downloaded [here](http://doi.org/10.5281/zenodo.4961965) for both individual A (ModelTime_A.csv) and B (ModelTime_B.csv).


### R code for the analysis - simulated data <br />

- The R code for the individual analysis, explained in Section 2, can be dowloaded [here](http://doi.org/10.5281/zenodo.4961965) (AB_individual.R). This code has been used to generate Figure 5.

- The R code for the dyadic analysis, explained in Section 2 and in our [SOF](https://ludovicalv.github.io/PDFs/Elep_paper.pdf), can be dowloaded [here](http://doi.org/10.5281/zenodo.4961965) (AB_pair.R). This code has been used to generate Figure 6.

- The R code used to plot the pair distance, colored according to the dyadic behaviour, can be downloaded [here](http://doi.org/10.5281/zenodo.4961965) (Col_distance_AB.R). This code has been used to generate Figures 7 and 8.

We used the integrated development environment [RStudio](https://rstudio.com/) to perform all the analysis.

### Empirical data: African elephant GPS relocation data <br />

The empirical relocation data will be provided should the manuscript be accepted.

### R code for the analysis - empirical data <br />

- The R code for the creation of the dataframe for the analysis (DataFrame_Pair.RData) can be dowloaded [here](http://doi.org/10.5281/zenodo.4928382) (DataFrame.R). 

- The R code for the individual analysis can be dowloaded [here](http://doi.org/10.5281/zenodo.4928382) both for the barplots (Ind_behaviour_barplot.R) and for the statistical analysis (Ind_behaviour_stat_analysis.R). This code has been used to generate Figure 9.

- The R code for the dyadic analysis can be dowloaded [here](http://doi.org/10.5281/zenodo.4928382) (Pair_analysis.R). This code has been used to generate Figure 10. 

- The R code for the extended analysis, explained in Section 2 and in our [SOF](https://ludovicalv.github.io/PDFs/Elep_paper.pdf), can be dowloaded [here](http://doi.org/10.5281/zenodo.4928382) (Extended_analysis.R). This code has been used to generate Figure 12.


