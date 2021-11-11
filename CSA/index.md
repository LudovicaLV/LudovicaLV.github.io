
## A comparison of COVID-19 outbreaks across US Combined Statistical Areas using new methods for estimating R_0 and social distancing <br />

R code and data for this paper can be found at this [repository](https://github.com/LudovicaLV/CSA_paper.git). The description of the files is the following:

### Day 0 <br />

We provide the R code to extract the day 0 of the exponential phase (CSA_day_0.R), by considering the first several weeks for which the 7-day lagged moving average was above 0 (CSA_av_above_0.R). We also provide the data folder for running this code (Data_CSA.zip), (data downloaded from https://usafacts.org/).

### R_0 <br />

To extract R_0 for each CSA, we provide the code to extract the exponential phase from the output of the SCLAIV model (CSA_exp_phase.R) and the code to calculate R_0 using the extracted data (Calc_R0.R). We also provide the population values for each CSA (csa_pop.xlsx) and all the output folder (Output.zip).

### Clustering <br />

To create the heatmap reported in the paper, we shared the code (CSA_heatmap.R) and the folder containing the curve flattening index for each CSA (Curve_CSA.zip).

### Curve flattening index: plots <br />

To create the three plots reported in the paper, we shared the code for the 20-day (CSA_plots_20_day.R) and 30-day length (CSA_plots_30_day.R).

### SOF1: additional clustering analysis <br />

To explore the additional clustering analysis, we provide the code for the heatmaps for the 4 area features and R_0 (CSA_heatmap_area4days_R0.R) and for the total area and R_0 (CSA_heatmap_area_R0.R). In addition, we provide the code for the silhouette analysis (CSA_silhouette.R) and for the scatter plots (Plot_clusters_points.R).
