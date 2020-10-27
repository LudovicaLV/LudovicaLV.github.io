## Supplementary material for the paper: <br />
## A relative-motion method for parsing spatio-temporal behaviour of dyads1using GPS relocation data <br />

Authors: [Ludovica Luisa Vissat](https://ourenvironment.berkeley.edu/people/ludovica-luisa-vissat), [Jason K. Blackburn](https://geog.ufl.edu/faculty/blackburn/), [Wayne M. Getz](https://ourenvironment.berkeley.edu/people/wayne-marcus-getz) <br />
l.luisavissat@berkeley.edu, jkblackburn@ufl.edu, wgetz@berkeley.edu

### Numerus Model Builder (NMB) models <br />

To generate the data used in Section 4, we defined and run the following NMB models, explained in details in our [SOF](https://ludovicalv.github.io/PDFs/Elep_paper.pdf). 

- The distance-dependent behaviour model (Model_distance.nmb) can be downloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM).

- The time-dependent behaviour model (Model_time.nmb) can be downloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM).

Visit [numerusinc.com](https://www.numerusinc.com/) to download the latest version of NMB.

### Simulated data: NMB output <br />

- The output of a simulation of the distance-dependent behaviour model can be downloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) for both individual A (ModelDistance_A.csv) and B (ModelDistance_B.csv).

- The output of a simulation of the time-dependent behaviour model can be downloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) for both individual A (ModelTime_A.csv) and B (ModelTime_B.csv).


### R code for the analysis - simulated data <br />

- The R code for the individual analysis, explained in Section 2 and 3, can be dowloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) (AB_individual.R). This code has been used to generate Figure 6.

- The R code for the pair analysis, explained in Section 2 and in our [SOF](https://ludovicalv.github.io/PDFs/Elep_paper.pdf), can be dowloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) (AB_pair.R). This code has been used to generate Figure 7.

- The R code used to plot the pair distance, colored according to the pair behaviour, can be downloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) (Col_distance_AB.R). This code has been used to generate Figures 8 and 9.

We used the integrated development environment [RStudio](https://rstudio.com/) to perform all the analysis.

### Empirical data: African elephant GPS relocation data <br />

The relocation data for the cow and the bull can be downloaded can be downloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) for both female (Cow.RData) and male (Bull.RData)

### R code for the analysis - empirical data <br />

- The R code for the creation of the dataframe for the analysis (calculation of pair distance and different angles of interest) can be dowloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) (DataFrame.R). Run this code as first step for any of the following analysis. Otherwise, download the output [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) (DataFrame_Pair.RData).

- The R code for the individual analysis can be dowloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) (Ind_behaviour_barplot.R) for the barplots and [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) (Ind_behaviour_stat_analysis.R) for the statistical analysis. This code has been used to generate Figure 10.

- The R code for the pair analysis can be dowloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) (Pair_analysis.R). This code has been used to generate Figure 11. 

- The R code for the extended analysis, explained in Section 2 and in our [SOF](https://ludovicalv.github.io/PDFs/Elep_paper.pdf), can be dowloaded [here](https://zenodo.org/record/4139757#.X5g4sXhKhsM) (Extended_analysis.R). This code has been used to generate Figure 15 .


