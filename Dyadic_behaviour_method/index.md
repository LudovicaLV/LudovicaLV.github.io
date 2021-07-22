## Supplementary material for the paper: <br />
## A relative-motion method for parsing spatio-temporal behaviour of dyads using GPS relocation data <br />

Authors: [Ludovica Luisa Vissat](https://ourenvironment.berkeley.edu/people/ludovica-luisa-vissat), [Jason K. Blackburn](https://geog.ufl.edu/faculty/blackburn/), [Wayne M. Getz](https://ourenvironment.berkeley.edu/people/wayne-marcus-getz) <br />
l.luisavissat@berkeley.edu, jkblackburn@ufl.edu, wgetz@berkeley.edu

All our material is stored in a Zenodo repository that can be found [here](http://doi.org/10.5281/zenodo.4961965). Note that the description and the names of the various files are provided in brackets on this webpage. 

### Numerus Model Builder (NMB) models <br />

To generate the data used in Section 3, we defined and simulated the following NMB models, explained in detail in our [SOF](https://ludovicalv.github.io/PDFs/Dyadic_behaviour_method_SOF.pdf). 

- The distance-dependent behaviour model (Model_distance.nmb) can be downloaded [here](http://doi.org/10.5281/zenodo.4961965).

- The time-dependent behaviour model (Model_time.nmb) can be downloaded [here](http://doi.org/10.5281/zenodo.4961965).

Visit [numerusinc.com](https://www.numerusinc.com/) to download the latest version of NMB.

### NMB output (simulated data) <br />

- The output of a simulation of the distance-dependent behaviour model can be downloaded [here](http://doi.org/10.5281/zenodo.4961965) for both individual A (ModelDistance_A.csv) and B (ModelDistance_B.csv).

- The output of a simulation of the time-dependent behaviour model can be downloaded [here](http://doi.org/10.5281/zenodo.4961965) for both individual A (ModelTime_A.csv) and B (ModelTime_B.csv).

### R code for the analysis - simulated data <br />

- The R code for the individual analysis, explained in Section 2, can be dowloaded [here](http://doi.org/10.5281/zenodo.4961965) (AB_individual.R). This code has been used to generate Figure 5.

- The R code for the dyadic analysis, explained in Section 2 and in our [SOF](https://ludovicalv.github.io/PDFs/Dyadic_behaviour_method_SOF.pdf), can be dowloaded [here](http://doi.org/10.5281/zenodo.4961965) (AB_pair.R). This code has been used to generate Figure 6.

- The R code used to plot the pair distance, colored according to the dyadic behaviour, can be downloaded [here](http://doi.org/10.5281/zenodo.4961965) (Col_distance_AB.R). This code has been used to generate Figures 7 and 8.

We used the integrated development environment [RStudio](https://rstudio.com/) to perform all the analysis.

### R Data frames (empirical data) <br />

- The data frames for each pair of interest can be downloaded [here](http://doi.org/10.5281/zenodo.4928382) (DataFrames.zip). 
Each data frame is named "DataFramex_y_z.RData", where x and y indicate the individual ID (see Tables 7-9 in [SOF](https://ludovicalv.github.io/PDFs/Dyadic_behaviour_method_SOF.pdf)) and z the data frequency. These data frames contain the pair distance, time stamps<sup>1</sup>, locations, absolute and relative headings and their difference for each individual. These values were calculated for each time point which was at the appropriate chosen frequency with respect to its consecutive time point. These data frames are the result of the calculations shown in Algorithm 1 in the main paper, before the classification step.

- In addition, we provide the data frame of the female-male pair of interest (DataFrame_Pair.RData), which contains also the calculated absolute heading difference and speed for both individuals. 

- The R code used for the creation of these data frames for the analysis can be dowloaded [here](http://doi.org/10.5281/zenodo.4928382) (DataFrame.R). 

### R code for the analysis - empirical data <br />

- The R code for the individual analysis can be dowloaded [here](http://doi.org/10.5281/zenodo.4928382) both for the barplots (Ind_behaviour_barplot.R) and for the statistical analysis (Ind_behaviour_stat_analysis.R). This code has been used to generate Figure 9.

- The R code for the dyadic analysis can be dowloaded [here](http://doi.org/10.5281/zenodo.4928382) (Pair_analysis.R). This code has been used to generate Figure 10. 

- The R code for the extended analysis, explained in Section 2 and in our [SOF](https://ludovicalv.github.io/PDFs/Dyadic_behaviour_method_SOF.pdf), can be dowloaded [here](http://doi.org/10.5281/zenodo.4928382) (Extended_analysis.R). This code has been used to generate Figure 12.

### Contact
- For any question regarding this project, please contact Ludovica Luisa Vissat (l.luisavissat@berkeley.edu)


<sup>1</sup> Note that the dates are in the numeric format. Please use the following R code to transform them in a date format, if needed: as.POSIXct(datenumeric, origin="1970-01-01", tz = "UTC")
