
## Supplementary material of the paper: <br />

## Analysis of spatio-temporal properties of stochastic systems using TSTL <br />

[Ludovica Luisa Vissat](http://homepages.inf.ed.ac.uk/s1372511/), [Michele Loreti](http://www.micheleloreti.com/), [Laura Nenzi](https://www.imtlucca.it/laura.nenzi), [Jane Hillston](	http://homepages.inf.ed.ac.uk/jeh), [Glenn Marion](	http://www.bioss.ac.uk/people/glenn.html)

### Three-Valued Spatio-Temporal (TSTL) properties verification: evacuation routes <br />

To analyse the TSTL property **<img src="http://latex.codecogs.com/svg.latex?\psi_{safe}">** (10 time units, r=2.0) presented in Fig. 3 in the paper: 

- Download [zip](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/PsiSafe.zip) file. 

- Run java -jar FireAnalysis.jar 

- The MATLAB file AnalysisPlot.m can be used to visualize the output of the analysis.

To analyse the TSTL property **<img src="http://latex.codecogs.com/svg.latex?\psi_{safeRoute}">** (t=0, r=2.0) presented in Fig. 4 in the paper: 

- Download [zip](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/GSafe.zip) file. 

- Run java -jar GSafe.jar 

- The MATLAB file AnalysisPlot.m can be used to visualize the output of the analysis.

- For different agent movement rates, r = 1.0 ([zip](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/GSafe1.zip) file), 3.0 ([zip](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/GSafe3.zip) file), 4.0 ([zip](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/GSafe4.zip) file)

### Reliability requirement  <br />

To apply the automatic procedure for the analysis of the TSTL property **<img src="http://latex.codecogs.com/svg.latex?\psi_{safeRoute}">** (t=0, r=4.0, k=10) presented in Fig. 6 in the paper:

- Download [zip](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/safeRouteRel.zip) file. 

- Run java -jar safeRoute.jar 

- The output will show the number of runs needed to satisfy each requirement. The MATLAB file AnalysisPlot.m can be used to visualize the output of the TSTL analysis at the given time point, inserting the correct file name, which will depend on the number of runs needed for each requirement (safeRoute_n.txt, where n is the number of runs, can be found in the first line of the MATLAB code).

To apply the automatic procedure for the analysis of the TSTL property **<img src="http://latex.codecogs.com/svg.latex?\psi_{fire}">** (t=5, k=10) presented in Fig. 7 in the paper:

- Download [zip](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/fireRel.zip) file. 

- Run java -jar fire.jar 

- The output will show the number of runs needed to satisfy each requirement. The MATLAB file AnalysisPlot.m can be used to visualize the output of the TSTL analysis at the given time point, inserting the correct file name, which will depend on the number of runs needed for each requirement (fire_n.txt, where n is the number of runs, can be found in the first line of the MATLAB code).

## Three-Valued Spatio-Temporal (TSTL) properties verification: anonymity network <br />

To analyse the TSTL property **<img src="http://latex.codecogs.com/svg.latex?\psi_{01}">** (20 time units) presented in Fig. 8, 9, 10, 11 in the paper: 

- Download zip file for the chosen scenario: <br />
[Scenario 1: basic scenario](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/basic.zip)  <br />
[Scenario 2: messages M0 5 time faster](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/5times.zip)  <br />
[Scenario 3: messages M0 10 time faster](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/10times.zip)   <br />
[Scenario 4: 50 initial messages for S0](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/50messages.zip)  <br />

- Run java -jar network01.jar 

- The Python file plot01.py can be used to visualize the output of the analysis of the TSTL property **<img src="http://latex.codecogs.com/svg.latex?\psi_{01}">**. The Python file plotM0.py can be used to visualize the output of the analysis, choosing the output file Scenario_n_M0.txt. Similarly, the Python file plotM1.py can be used to visualize the output of the analysis choosing Scenario_n_M1.txt. 

- Once the previous simulations have been performed, the Python file plotTotal.py can be used to visualize the output of the analysis of the TSTL property **<img src="http://latex.codecogs.com/svg.latex?\psi_{total}">** (20 time units) presented in Fig. 12 in the paper. The results have been produced choosing any of the scenarios presented earlier and the output file for this result is called Scenario_n_TOTAL.txt

## Additional material (videos) <br />
We provide the spatio-temporal evolution of TSTL properties related with the case study on emergency evacuation route presented in the paper. <br />

[Safe exit (r=2.0)](https://ludovicalv.github.io/Videos/SafeExit_Rate2))  <br />
<video src="https://ludovicalv.github.io/Videos/SafeExit_Rate2" width="320" height="200" controls preload></video>

[Safe exit (r=4.0)](https://drive.google.com/open?id=0B6Jk3sy4LnqwZ254NFF3d1U2VTg)  <br />
[Fire spread](https://drive.google.com/open?id=0B6Jk3sy4LnqwMnppWEc2YjJaeEU)  <br />

### Additional material (MELA models)
We present the [MELA](https://arxiv.org/abs/1610.08171) models we used to perform stochastic simulations.<br />

Case study: Emergency evacuation route<br />
[MELA model safe exit](https://ludovicalv.github.io/MELA2/)<br />

Case study: Anonymity network<br />
[Basic Scenario](https://ludovicalv.github.io/Basic/)<br />
[Messages M0 move 5 time faster](https://ludovicalv.github.io/5Faster/)<br />
[Messages M0 move 10 time faster](https://ludovicalv.github.io/10Faster/)<br />
[Sender S0 has 50 initial messages](https://ludovicalv.github.io/50Initial/)<br />
