# Synthetic GPR models

For Exercise 3, you will need to run synthetic GPR models, observe the results, and respond to regarding these observations.

For synthetic GPR data, we will run gprMax, an open-source electromagnetic modeling software. The gprMax software can be difficult to set up, so this readme provides instructions for setting up gprMax in a Github codespace. Follow the instructions below to install and run gprMax.

# Setup and run gprMax for synthetic GPR modeling
1. Create a Github codespace from the Geol451 Repository
  a) Go to the main [GEOL451 github repository page](https://github.com/RJbalikian/GEOL451)
  b) There should be a (green) button near the top right of the main page that says "<> Code" ![GEOL451Repo with Green Code Button](image.png)
  c) Click the Code button, navigate to the "Codespaces" tab, select the "+" button to create a codespace (remember, a codespace is essentially a virtual computer where you can run code on a Microsoft/Github system)
2. Use the Explorer tab (icon looks like two pages) on the left side of your browser window (or click Ctrl + Shift + E) 
  a) Your "Home" directory in this codespace will be "/workspaces/GEOL451/"
  b) Navigate to the GPR Folder in your codespace. You can continue to read these instructions are located in the Readme file at /workspaces/GEOL451/GPR/Readme.md
3. The lower half of your page should by default have a bash terminal window. There are multiple "tabs" on the top of this section should have multiple views. Select the "Terminal" view. At the right side of this window section is a "plus" button and chevron (down arrow). It should say bash next to that, and your terminal should have your username and your current directory and the branch name in parantheses. For me, this looks like: "@RJbalikian ➜ /workspaces/GEOL451 (main) $". Your cursor should be after the $.
  ![Default bash terminal in GEOL451](image-1.png)
4. We will install gprMax and work with it from here. In the terminal, change your directory to the GPRMax directory using the follow command: `cd GPR/GPRMax`
