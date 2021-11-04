
## R code and data for the paper: A comparison of COVID-19 outbreaks across US Combined Statistical Areas using new methods for estimating $R_0$ and social distancing <br />

### Day 0 <br />

We provide the R code to extract the day 0 of the exponential phase (CSA_day_0.R), by considering the first several weeks for which the 7-day lagged moving average was above 0 (CSA_av_above_0.R). We also provide the data folder for running this code (CSA folder).

### R_0 <br />

To extract R_0 for each CSA, we provide the code to extract the exponential phase from the output of the SCLAIV model (exp phase.R) and the code to calculate R_0 using the extracted data. We also provide the population values for each CSA (.xlsx) and all the output folder (.zip).

### Clustering <br />

To create the heatmap reported in the paper, we shared the code (.R) and the folder containing the curve flattening index for each CSA (.zip).

### Curve flattening index: plots <br />

To create the three plots reported in the paper, we shared the code for the 20-day (.R) and 30-day length (.R).
