# GPR Analysis
# Introduction
The process of acquiring and analyzing Ground Penetrating Radar (GPR) data is composed of several steps:
1. Survey Design
2. Data acquisition
3. Preprocessing
4. Data Processing/Analysis
5. Data Interpretation
6. Dissemination of results

We have already covered steps 1, 2, and 3. Here, we will go over step 4 (Data processing/analysis).

We will use a python package called GPRpy to analyze this data. 
While it has a graphical user interface (GUI), here we will use the python interface.
Towards this end, a jupyter notebook (GEOL451_GPRProcessing.ipynb) has been provided tha will walk you through the GPR processing steps.

The remainder of this document will help you set up your environment to run GPRpy and learn about and carry out standard GPR Processing steps on a real-world dataset.

# Setup and Install GPRpy
These instructions will walk you through how to set up GPRpy to be run in the current folder (GEOL451/GPR/GPRProcessing).
This can be done on Github Codespaces or on your local machine.
These instructions are drawn heavily from the official [GPRpy Github Repository Readme](https://github.com/NSGeophysics/GPRPy/tree/master)

## GPRpy Installation
1. Install git
    * This can be installed from [git's website](https://git-scm.com/downloads) or...
    * This can be install with anaconda: `conda install git` (recommended for github codespaces, takes about 30 sec)
2. Change the working directory of your terminal to GPRProcessing:
    * In codespaces/terminal: `cd ./GPR/GPRProcessing/`
    * (You can clone the repository to a difference directory, but the Jupyter notebook you will run needs to be in the same folder as the top-level folder of the GPRpy directory)
3. Clone the GPRpy repository to this GPRProcessing folder (<10 seconds)
    * `git clone https://github.com/NSGeophysics/GPRPy.git`
4. Change your working directory againg to the top-level GPRPy folder
    * `cd GPRPy`
5. Pre-installation setup (<10 seconds)
    * `python installMigration.py`
6. Install GPRPy
    * `pip install .` (NOTE: you must includ the period (.) at the end of your command)

Steps 1-7 as a code bloc:
```bash
conda init
# KILL TERMINAL
# REOPEN TERMINAL (Ctrl + `)
conda env -n gprpy
conda activate gprpy
conda install git
conda install setuptools
cd ./GPR/GPRProcessing
git clone https://github.com/NSGeophysics/GPRPy.git
cd GPRPy
python installMigration.py
pip install .
```

Open the jupyter notebook and begin processing! GEOL451_GPRProcessing.ipynb
