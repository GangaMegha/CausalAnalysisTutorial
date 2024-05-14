# Causal Insights From Observational Data: A Hands-On Python Workshop

Welcome to the GitHub repository for the Causal Analysis Workshop at the Women in Data Science (WiDS) conference, May 2024, Puget Sound (https://www.widspugetsound.org/2024-schedule). 

This workshop is designed to introduce the basic concepts and methods of causal discovery and causal inference. 

## Overview

Causal analysis is a powerful tool for understanding the mechanisms and effects of interventions in complex systems. While A/B experimentation is the gold standard for extracting causal insights, there are situations where experimenting isn’t possible – such as when the feature was already released or ethical restrictions prevent us from experimenting on certain populations. 

In such cases, we must rely on observational data, which pose many challenges for causal analysis, such as confounding, selection bias, and unmeasured variables. 

In this workshop, we will guide the audience through a hands-on, step-by-step causal analysis using common Python causal libraries, including DECI and EconML. 

## Requirements

- An internet-connected device
- Basic knowledge of Python

## Getting started

1. Use ```git clone https://github.com/GangaMegha/CausalAnalysisTutorial.git``` to clone this repository on to your system.
2. Navigate to the directory using ``` cd CausalAnalysisTutorial ```.
3. Setup your environment and install the libraries ( Go to Environment-Setup )
4. Launch Jupyter Notebook using ```jupyter notebook```.
5. Click and open the notebook **WiDsCausalAnalysisWorkshop.ipynb**.
6. You're all set to go!

## Environment-Setup
You will need to install the necessary python packages to do causal analysis using DECI and DML in the hands-on workshop. 

It is recommended that you create and work within a virtual environment to avoid package conflicts with other libraries you have installed on your machine. 

[!IMPORTANT]
Please use [Python 3.10](https://www.python.org/downloads/release/python-31011/) for this tutorial.

### Option 1: Python virtual environment

Install the virtual environment package if it’s not already installed using ```pip install virtualenv```

Create the environment:

Try: 
```
python3.10 -m venv env_causal
```

If the above does not work for you, find the path to the Python interpreter of the version you want to use with ``` where python ``` and create environment using 
``` 
virtualenv -p path_to_python env_causal 
```

Activate your environment:
- Windows: ```env_causal\Scripts\activate```
- Unix or MacOS: ```source env_causal/bin/activate```

### Option 2: Conda environment

Use if you already have anaconda installed on your machine.

```
conda create --name env_causal python=3.10 -y
```
Activate your environment:```conda activate env_causal```

### Option 3: Docker container

```bash
# Run this command line from the repo root folder
# Then open http://localhost:8888/lab from your browser in the host

docker run --rm -p 8888:8888 -v .:/home/jovyan jupyter/scipy-notebook:python-3.10
```


## Packages

You can install all the packages in a Python 3.10 environment using 
```
pip install -r requirements.txt
```
Or install the dependencies from the notebook using

```
!pip install -r requirements.txt
```

The above will install all necessary packages for the workshop on your system with the correct versions. This will help avoid any version conflicts.

-OR-

If you already have a python environment created to run jupyter notebooks, you can also install the below packages individually:
1. **DECI** [https://github.com/microsoft/causica] : ```pip install causica```
2. **DML** [https://econml.azurewebsites.net/spec/estimation/dml.html]: ```pip install econml```


## Dataset

We will use the same toy dataset used in DECI and EconML (Multi-investment Attribution) for illustration. The dataset and related files can be found in the `data` directory of this repository.
