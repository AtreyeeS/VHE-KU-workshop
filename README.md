# Gammapy tutorials for VHE Data Analysis Using Open Source Packages

## Installation and set-up 

We reccomend that you install gammapy via conda (or alternatively use mamba)

- $ curl -O https://gammapy.org/download/install/gammapy-0.19-environment.yml
- $ conda env create -f gammapy-0.19-environment.yml
- $ conda activate gammapy-0.19

To download the tutorials and associated datasets (necessary for the tutorials in this workshop)

- $ gammapy download notebooks --release 0.19
- $ gammapy download datasets
- export GAMMAPY_DATA=$PWD/gammapy-datasets

To check if everything is working fine, open a new terminal and type

- $ conda activate gammapy-0.19
- $ ipython

In the ipython window, type
- from gammapy.data import DataStore
- ds = DataStore.from_dir("$GAMMAPY_DATA/hess-dl3-dr1")
- obs = ds.get_observations()
- print(len(obs))

If the cells run without any error and prints `105`, **Congratulations! You have correctly set-up gammapy**

## Tutorials to be shown
- loading observations and IRFs
- Data reduction and fitting of MSH 15-52 (a full analysis)
- Simulation of PKS 2155-304 with CTA IRFs
- Fitting of simulated PKS 2155-304: detection significance, detection of cutoff
- Fitting of simulated PKS 2155-304: joint Fermi-LAT and CTA fitting
- Light curves.
