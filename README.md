### Overview
This repository provides the code to reproduce my master thesis "Simulation-based comparison of Bayesian inference methods in hierarchical Bayesian models". `simulation.R` simulates the temporal discounting task and creates the folder `out/` with its folder structure. For each sample, `params.rds` is saved, which includes the parameter values used for simulation of each subject. `data.rds` includes the information about each trial and the choices in long format. After simulating, hierarchical Bayesian models can be fitted to the data of each sample with `modeling.R`, which creates the model files containing model parameter estimates within each samples folder. Stan model files can be found in `models/`. The `analysis.R` file computes the data frame `results.rds`, which for each model includes the sample number, prior standard deviation, population effect standard deviation, values of Bayesian inference methods, and dummy-coded variables indicating whether conventional and simulation-based decision thresholds produced false positive conclusions (1) or not (0). Simulation-based decision thresholds are saved in `sim_thres.rds`.  All plots can be created with `plots.R`. The results section was written in R Markdown. Knitting `results.Rmd` produces a HTML file with the LaTeX code to produce the results section.