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
1. Initiate conda and restart your terminal
    * `conda init`
    * Kill the terminal by clicking the trash can icon near the top-right of your lower terminal window
    * Restart the terminal by type Ctrl + ` (grave accent, on same key as tilde (~) usually)
2. Create and activate an anaconda environment called gprpy that we will install gprpy into
    * `conda create -n gprpy`
    * `conda activate gprpy`
3. Install git and setuptools, use the following commands in your terminal:
    * `conda install git` installs git directly into the anaconda environment. This is recommended for github codespaces, takes about 30 sec.
        * If you are doing this on your local computer, you can also install directly from the [git website](https://git-scm.com/downloads)
    * `conda install setuptools` will install the setuptools package that anaconda can use to set up gprpy
4. Change the working directory of your terminal to GPRProcessing:
    * In codespaces/terminal: `cd ./GPR/GPRProcessing/`
    * (You can clone the repository to a difference directory, but the Jupyter notebook you will run needs to be in the same folder as the top-level folder of the GPRpy directory)
5. Clone the GPRpy repository to this GPRProcessing folder (<10 seconds)
    * `git clone https://github.com/NSGeophysics/GPRPy.git`
6. Change your working directory againg to the top-level GPRPy folder
    * `cd GPRPy`
7. Pre-installation setup to install the migration toolset (<10 seconds)
    * `python installMigration.py`
8. Install GPRPy
    * `pip install .` (NOTE: you must include the period (.) at the end of your command)

Steps 1-7 as a code block:
```bash
conda init
# KILL TERMINAL (trash can icon near top right of lower terminal window)
# REOPEN TERMINAL (Ctrl + `)
conda create -n gprpy
conda activate gprpy
conda install git setuptools
cd ./GPR/GPRProcessing
git clone https://github.com/NSGeophysics/GPRPy.git
cd GPRPy
python installMigration.py
pip install .
```

Open the jupyter notebook (GEOL451_GPRProcessing.ipynb) and begin processing!
* Remember, if you are using a fresh Github Codespace, you must first install the python and jupyter extensions, and select the gprpy kernel!

If modules are not importing correctly, you may need to move your Jupyter Notebook into the GPRPy folder.
