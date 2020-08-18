## Supplementary material for the paper: <br />
## A method for parsing spatio-temporal features of dyadic movement behaviour using GPS relocation data <br />

Authors: [Ludovica Luisa Vissat](https://ourenvironment.berkeley.edu/people/ludovica-luisa-vissat), [Wayne M. Getz](https://ourenvironment.berkeley.edu/people/wayne-marcus-getz) <br />
Depart. ESPM, University of California, Berkeley, CA 94720-3114, USA <br />
l.luisavissat@berkeley.edu, wgetz@berkeley.edu

### Numerus Model Builder (NMB) models <br />

To generate the data used in Section 4, we defined and run the following NMB models, explained in details in our [SOF](https://ludovicalv.github.io/PDFs/Elep_paper.pdf). 

- The distance-dependent behaviour model can be downloaded [here](https://www.dropbox.com/s/ufdlxob30kth802/Model_distance.nmd?dl=1).

- The time-dependent behaviour model can be downloaded [here](https://www.dropbox.com/s/sk9k1kmb26vjwxr/Model_time.nmd?dl=1).

Visit [numerusinc.com](https://www.numerusinc.com/) to download the latest version of NMB.

### Simulated data: NMB output <br />

- The output of a simulation of the distance-dependent behaviour model can be downloaded [for individual A](https://www.dropbox.com/s/sm8u2rwc844snz3/ModelDistance_A.csv?dl=1) and [for individual B](https://www.dropbox.com/s/8wv0pk2jlq45qq1/ModelDistance_B.csv?dl=1).

- The output of a simulation of the time-dependent behaviour model can be downloaded [for individual A](https://www.dropbox.com/s/hzu2rfv919r96um/ModelTime_A.csv?dl=1) and [for individual B](https://www.dropbox.com/s/s8ffj1jvrlkqitp/ModelTime_B.csv?dl=1).


### R code for the analysis - simulated data <br />

- The R code for the individual analysis, explained in Section 2 and 3, can be dowloaded [here](https://www.dropbox.com/s/0ny86eiz8j1uc4s/AB_individual.R?dl=1). This code has been used to generate Figure 6.

- The R code for the pair analysis, explained in Section 2 and in our [SOF](https://ludovicalv.github.io/PDFs/Elep_paper.pdf), can be dowloaded [here](https://www.dropbox.com/s/9qn0j0bh4mp8b1b/AB_pair.R?dl=1). This code has been used to generate Figure 7.

- The R code used to plot the pair distance, colored according to the pair behaviour, can be downloaded [here](https://www.dropbox.com/s/2swvlqvb56qc33j/Col_distance_AB.R?dl=1). This code has been used to generate Figures 8 and 9.

We used the integrated development environment [RStudio](https://rstudio.com/) to perform all the analysis.

### Empirical data: African elephant GPS relocation data <br />

The relocation data for the cow and the bull can be downloaded can be downloaded: [cow](https://www.dropbox.com/s/s0pn4wwbo6lfv57/Cow.RData?dl=1), [bull](https://www.dropbox.com/s/lzkjqjjfm4t4gi0/Bull.RData?dl=1)

### R code for the analysis - empirical data <br />

- The R code for the creation of the dataframe for the analysis (calculation of pair distance and different angles of interest) can be dowloaded [here](https://www.dropbox.com/s/mf6tervxxa71krg/DataFrame.R?dl=1). Run this code as first step for any of the following analysis. Otherwise, download the output [here](https://www.dropbox.com/s/d3wscbfzwpv1a21/DataFrame_Pair.RData?dl=1).

- The R code for the individual analysis can be dowloaded [here](https://www.dropbox.com/s/8yvxon8w0f9hix2/Ind_behaviour_barplot.R?dl=1) for the barplots and [here](https://www.dropbox.com/s/qpybdb7nmyr6snp/Ind_behaviour_stat_analysis.R?dl=1) for the statistical analysis. This code has been used to generate Figure 10.

- The R code for the pair analysis can be dowloaded [here](https://www.dropbox.com/s/tq51brvk9sk1qcf/Pair_analysis.R?dl=1). This code has been used to generate Figure 11. 

- The R code for the extended analysis, explained in Section 2 and in our [SOF](https://ludovicalv.github.io/PDFs/Elep_paper.pdf), can be dowloaded [here](https://www.dropbox.com/s/lklrq5mabevw62x/Extended_analysis.R?dl=1). This code has been used to generate Figure 15 .


