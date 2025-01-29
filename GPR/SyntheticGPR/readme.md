# Synthetic GPR models

For Exercise 3, you will need to run synthetic GPR models, observe the results, and respond to several questions regarding these observations.

For synthetic GPR data, we will run gprMax, an open-source electromagnetic modeling software. The gprMax software can be difficult to set up, so this readme provides instructions for setting up gprMax in a Github codespace. Follow the instructions below to install and run gprMax.


# Setup gprMax for synthetic GPR modeling
1. Create a Github codespace from the Geol451 Repository
  a) Go to the main [GEOL451 github repository page](https://github.com/RJbalikian/GEOL451)
  b) There should be a (green) button near the top right of the main page that says "<> Code" ![GEOL451Repo with Green Code Button](image.png)
  c) Click the Code button, navigate to the "Codespaces" tab, select the "+" button to create a codespace (remember, a codespace is essentially a virtual computer where you can run code on a Microsoft/Github system)
2. Use the Explorer tab (icon looks like two pages) on the left side of your browser window (or click Ctrl + Shift + E) 
  a) Your "Home" directory in this codespace will be "/workspaces/GEOL451/"
  b) Navigate to the GPR Folder in your codespace. You can continue to read these instructions here, but they are also located in the Readme file at /workspaces/GEOL451/GPR/SytheticGPR/Readme.md
3. The lower half of your page should by default have a bash terminal window. There are multiple "tabs" on the top of this section should have multiple views. Select the "Terminal" view (this should be selected by default). At the right side of this window section is a "plus" button and chevron (down arrow). It should say bash next to that, and your terminal should have your username and your current directory and the branch name in parantheses. For me, this looks like: `@RJbalikian ➜ /workspaces/GEOL451 (main) $`. Your cursor should be after the $.
  ![Default bash terminal in GEOL451](image-1.png)

## You can skip the rest of the numbered section if you would just like to see the commands you will perform in the terminal. It is shown as a code block below (but you should run each line individually)
### If you run these commands without any issues, it takes a little less than 10 minutes to install on Github codespaces


4. We will install gprMax and work with it from here. First, we will initialize anaconda. Run `conda init`.
5. After you initialize anaconda, you will need to kill your terminal then reopen it.
  i) KILL YOUR TERMINAL (click the trash can icon/kill terminal button near the top right of the lower/terminal window)
  ii) REOPEN YOUR TERMINAL. The easiest way is Ctrl + Grave Accent (this is usually the button (which also has a tilde ~ on it) next to the 1 at the top left of your keyboard)
6. Now in your new terminal, change your directory to the GPRMax directory using the follow command: `cd GPR/SyntheticGPR/GPRMax`
7. We will install gprMax into this folder using anaconda (this should already be installed on your codespace). The instructions for this are included here, but you may also see more information at the gprMax documentation [here](https://docs.gprmax.com/en/latest/include_readme.html#installation). You may have to type "y" when the system prompts to confirm that you want to install/download based on these commands. Usually, you have to right click and select paste if you are copy/pasting these commands (Ctrl + v may not work)
  i) Your terminal should now say: `@<YOUR_USERNAME> ➜ .../GEOL451/GPR/SyntheticGPR/GPRMax (main) $`. 
  ii) Add the conda-forge channel to anaconda: `conda config --append channels conda-forge`
  iii) Update anaconda: `conda update conda` (this takes about 30-60 seconds, you will need to type y then press enter to confirm along the way)
  iv) Install git (to be able to copy the gprMax package to your codespace): `conda install git` (30 seconds or so)
  v) Clone/copy the gprMax repository into your GPRMax folder: `git clone https://github.com/gprMax/gprMax.git` (10-20 seconds)
  vi) Change your working directory into your new gprMax folder: `cd gprMax`
  vii) Create a new anaconda environment with all the dependencies needed to run gprMax: `conda env create -f conda_env.yml` (1-2 minutes)
  xi) Activate the gprMax anaconda environment: `conda activate gprMax`
    a) You should notice the environment name at the far left of your terminal `(gprMax)`
  xii) Build the gprMax software package: `python setup.py build` (1-2 minutes)
  xiii) Install the gprMax software package: `python setup.py install` (10-30 seconds)

To repeat and display in a more compact form, these commands are:
```bash
conda init
# KILL YOUR TERMINAL
# REOPEN THE TERMINAL
cd GPR/SyntheticGPR/GPRMax
conda config --append channels conda-forge
conda update conda
conda install git
git clone https://github.com/gprMax/gprMax.git
cd gprMax
conda env create -f conda_env.yml
conda activate gprMax
python setup.py build
python setup.py install
```

# Run gprMax
After you have built and installed gprMax, we will do calculations and run gprMax from a jupyter notebook.

The notebook you will run (and which has all the instructions you need for exercise 3) is located in the following directory: GPR/SyntheticGPR/GEOL451_GPRMaxFiles. It is called GEOL451_Ascan_250MHz_2d.ipynb

