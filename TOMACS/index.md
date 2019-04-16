
## Supplementary material of the paper: Analysis of spatio-temporal properties of stochastic systems using TSTL <br />

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

- The output will show the number of runs needed to satisfy each requirement. The MATLAB file AnalysisPlot.m can be used to visualize the output of the TSTL analysis at the given time point, inserting the correct file name in the MATLAB file (in the first line). The name, safeRoute_n.txt, will depend on the output, where n is the number of runs needed for each requirement.

- The output Result.txt will show the number of simulations and the number of U values of the corresponding analysis.

To apply the automatic procedure for the analysis of the TSTL property **<img src="http://latex.codecogs.com/svg.latex?\psi_{fire}">** (t=5, k=10) presented in Fig. 7 in the paper:

- Download [zip](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/FireRel.zip) file. 

- Run java -jar Fire.jar 

- The output will show the number of runs needed to satisfy each requirement. The MATLAB file AnalysisPlot.m can be used to visualize the output of the TSTL analysis at the given time point, inserting the correct file name in the MATLAB file (in the first line). The name, fire_n.txt, will depend on the output, where n is the number of runs needed for each requirement.

- The output Result.txt will show the number of simulations and the number of U values of the corresponding analysis.


### Three-Valued Spatio-Temporal (TSTL) properties verification: anonymity network <br />

To analyse the properties presented in Fig. 8-12 in the paper: 

- Download zip file for the chosen scenario: <br />
[Scenario 1: basic scenario](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/Scenario1.zip)  <br />
[Scenario 2: messages M0 5 time faster](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/Scenario2.zip)  <br />
[Scenario 3: messages M0 10 time faster](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/Scenario3.zip)   <br />
[Scenario 4: 50 initial messages for S0](https://github.com/LudovicaLV/EvacuationRoutes_Analysis/releases/download/V0.1beta/Scenario4.zip)  <br />

- Run java -jar Scenario_n.jar, choosing the appropriate n, between 1, 2, 3, 4, depending on the scenario. 

- Figures 8-11: the Python file plot01.py can be used to visualize the output of the analysis of the TSTL property **<img src="http://latex.codecogs.com/svg.latex?\psi_{01}">**, while the Python files plotM0.py and plotM1.py can be used to visualize the output of the analysis, looking at the estimated satisfaction probabilities of the relative SSTL properties. 
- Figure 12: the Python file plotTotal.py can be used to visualize the output of the analysis of the TSTL property **<img src="http://latex.codecogs.com/svg.latex?\psi_{total}">**. 

### Additional material (videos) <br />
We provide the spatio-temporal evolution of TSTL properties related with the case study on emergency evacuation route presented in the paper. <br />

[Safe exit (r=2.0)](https://www.youtube.com/watch?v=XM7qFoLOGkE&feature=youtu.be)  <br />
[Safe exit (r=4.0)](https://www.youtube.com/watch?v=5uY1Ovamf3Y&feature=youtu.be)  <br />
[Fire spread](https://www.youtube.com/watch?v=qSEIFJx_DhM&feature=youtu.be)  <br />

### Additional material (MELA models)
We present the [MELA](https://arxiv.org/abs/1610.08171) models we used to perform stochastic simulations.<br />

Case study: Emergency evacuation route<br />
[MELA model safe exit](https://ludovicalv.github.io/MELA2/)<br />

Case study: Anonymity network<br />
[Basic Scenario](https://ludovicalv.github.io/Basic/)<br />
[Messages M0 move 5 time faster](https://ludovicalv.github.io/5Faster/)<br />
[Messages M0 move 10 time faster](https://ludovicalv.github.io/10Faster/)<br />
[Sender S0 has 50 initial messages](https://ludovicalv.github.io/50Initial/)<br />
