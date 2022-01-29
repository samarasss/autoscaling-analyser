# Autoscaling-analyser

### Purpose
The purpose of this project is to analyse auto-scaling strategies based on the
ADI metric proposed by Marco A. S. Netto on the "Evaluating Auto-scaling Strategies for Cloud Computing Environments" article. The implementation was developed based on the rules and parameters of the article.

### Auto-scaling Demand Index

The Auto-scaling Demand Index (ADI) as quoted by Marcos 

> "is the sum of all distances computed between each utilisation level reported by the system and the target utilisation interval set by the user. [...] ADI is convenient because it employs the same metric to evaluate (or, more precisely, penalise) both
unacceptable QoS and resource underutilisation."

### Installation

You can install R software for free [here](https://www.r-project.org/).
Install the following library dependencies, on R console:
```
> install.packages("dplyr", "testthat")
```
Or you can install under the "packages" tab on R Studio.

### Usage

The [main.R](https://github.com/ufcg-lsd/autoscaling-analyser/blob/samara/src/main.R) file is where you want to start playing with the algorithm. 
You can add new data files, or you can use the one that we offer as sample: 
[decreasing_data.csv](https://github.com/ufcg-lsd/autoscaling-analyser/blob/samara/data/decreasing_data.csv)

You can run the script on your terminal on the repo root directory, with the following command:
```
$ R -f src/main.R
```
Or instead, we recommend you to use [RStudio IDE](https://www.rstudio.com/products/rstudio/download/)
which has all the tools you need to develop using R.


### Organization of the repo
```
├── data/
│   System monitoring data files that you want to evaluate.
├── src/
│   The ADI Evaluation algorithm
│   └── policies/
│       Auto-scaling policies algorithms
└── tests/
    Test cases to check if the algorithm is working as expected
```
