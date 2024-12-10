---
title: "My_Project.md"
author: "First Last"
date: "2023-12-01"
output: github_document
---
# Title of My Project
   
## Background/Overview

Describe here the background and motiviation for completing this project.

References:
* Link 1
* Link 2
* Link 3

## Project Aims
Aim 1: 

Aim 2:

## Analysis Plan

#### Data Preprocessing

* Step 1: Link to script. 
* Step 2: Link to script.

#### Aim 1
* Analysis 1: We will use this software: ____  to do ____.
  
 Link to script here.

* Analysis 2: We will write custom code to ____.
  
 Link to script here. 

#### Aim 2
* Analysis 1
* Analysis 2

#### Interpretation
* Data visualization: We will use ggplot in R to make plots.

## Data Structure

Project directory: 

Tree diagram for data, code, outputs within the project directory. 

```bash
project_directory # The working directory
├── data
│   ├── raw_data.csv 
│   └── processed_data.csv 
├── output
│   ├── results 
│   │     ├── results_aim_1.csv # write a note about what this file contains.
│   │     └── results_aim_2.csv
│   └── visualization 
│         └── plots_aim_1.png
│         └── plots_aim_2.png
└── scripts 
    ├── data_processing.Rmd
    ├── analyses_aim_1.1.sh
    ├── analyses_aim_1.2.Rmd
    ├── analyses_aim_2.1.py
    └── data_visualziation.Rmd
```

## Expected Results

Describe your expected results here. 

If the project is completed, describe the format, location of output data.

## Responsibilities and Acknowledgements

Caroline is responsible for data preprocessing. Ale will conduct analyses described in Aim 1. Jake will perform analyses in Aim 2. Alexis will perform data visualization. 

This work is funded by the following grants:
* Grant 1
* Grant 2

## Software Installation
(Adapted from [LeafCutter installation instructions](https://davidaknowles.github.io/leafcutter/articles/Installation.html)) \
\
The prerequisites for LeafCutter are: \
	- samtools should be available on your PATH \
	- regtools should be available on your PATH \
	- Python 2.7 (earlier versions may be OK) \
	- R (version 3.6.0, earlier versions may be OK) \
 \
To download the code (you’ll need this for the leafcutter scripts):
  ```bash
git clone https://github.com/davidaknowles/leafcutter
  ```
To check if software is available on your PATH:
  ```bash
echo $PATH
   ```
To add software to your PATH:
```bash
export $PATH=$PATH:/path/to/software

# For example, adding regtools to PATH:
export $PATH=$PATH:/home/mac/jkhan1/bin/regtools/build
   ```
### Installing rstan
Leafcutter relies on stan and its R interface rstan. Installing this can be tricky. If you’re lucky, this will work:
```bash
install.packages("rstan")
```
For now we also need a version of rstantools (2.0.0) that is not yet on CRAN, so do:

```bash
if (!require("devtools")) install.packages("devtools", repos='http://cran.us.r-project.org')
devtools::install_github("stan-dev/rstantools")
```
### Using devtools (recommended)
To compile the R package to perform differential splicing analysis and make junction plots we recommend you install using devtools (this should install the required R package dependencies for you).

```bash
devtools::install_github("davidaknowles/leafcutter/leafcutter")
```

We’ve had a report (thanks to Peter Carbonetto) that it may be necessary to restart R before trying to load leafcutter because dplyr may get updated during the installation process.

