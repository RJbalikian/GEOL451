# GEOL 451 
# Electrical Resistivity Tomography (ERT) Module
> This folder has all the data and information needed for the ERT module

The following will walk you through how to set up your environment Github Codespaces. 
You can follow similar steps to set up a local machine as well.

We have run operations line-by-line in the past to setup our environment. 

Now, we are going to practice using preconfigured files to setup and install everything at once.

### Steps for installing resipy:
1) Open a Github Codespace
2) Linux machines (i.e., Github Codespaces) need WINE installed to run resipy. 
    * On Github Codespaces, a few setup steps need to be done:
        * Add and verify a download source for your package installation manager (called apt)
        * Add flexibility to the type of program that can be installed on your system. 
        * This requires 6 steps laid out in the `ert_ghcs_setup.sh` shell script file.
        * You can just run that file using the `source` command to do that automatically.
    * Run in your terminal: `source "/workspaces/GEOL451/ERT/ert_ghcs_setup.sh"`
        * This will take a minute or two to run
3) Install the necessary python modules in whichever environment you are using
    * The names of the needed modules are stored in a .txt file You can install these using the below command:
    * You can open the file itself to view the modules to be installed, which are pandas, resipy, ipykernel, and ipywidgets
    * Run in your terminal: `pip install -r "/workspaces/GEOL451/ERT/ert_requirements.txt"`

As a simple code block, it's just two commands:
```bash
source "/workspaces/GEOL451/ERT/ert_ghcs_setup.sh"
pip install -r "/workspaces/GEOL451/ERT/ert_requirements.txt"
```

Now you are ready to run the jupyter notebooks in the ERT folder and subfolders.

These Jupyter notebook contains all the instructions you should need to carry out your assignments.
