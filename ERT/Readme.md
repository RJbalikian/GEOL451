# GEOL 451 
# Electrical Resistivity Tomography (ERT) Module
> This folder has all the data and information needed for the ERT module

The following will walk you through how to set up your environment Github Codespaces. 
You can follow similar steps to set up a local machine as well.

Steps:
1) Open a Github Codespace
2) Install the necessary python modules in whichever environment you are using
    * You can install the modules listed in the ert_requirements.txt file using the below command:
    * `pip install -r "/workspaces/GEOL451/ERT/ert_requirements.txt"`
       * This modules are pandas, resipy, ipykernel, and ipywidgets
3) Linux machines only (i.e., Github Codespaces), run the following commands in order in your terminal:
    * sudo mkdir -pm755 /etc/apt/keyrings
    * wget -O - https://dl.winehq.org/wine-builds/winehq.key | sudo gpg --dearmor -o /etc/apt/keyrings/winehq-archive.key -
    * sudo wget -NP /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/focal/winehq-focal.sources
    * sudo dpkg --add-architecture i386 
    * sudo apt update
    * sudo apt install -y wine64 wine32
        * (This last step takes a few minutes to run)

Now you are ready to run the jupyter notebook.

This Jupyter notebook contains all the instructions you should need to carry out the rest of your assignment.
