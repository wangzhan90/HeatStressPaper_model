# Heat Stress Paper: Model for Simulations
By: Zhan Wang, Department of Agricultural Economics, Purdue University.

Contact: zhanwang@purdue.edu
# Introduction
This repository contains the source code, experiments and database of the Simplified International Model of agricultural Prices, Land use, and the Environment - Gridded version (SIMPLE-G) for simulating the impact of human heat stress on US agriculture. 

This model was originally developed for the I-GUIDE summer school (IGS) by Iman Haqiqi. Zhan Wang further updated this model by extending the non-land input to the composite of labor and capital inputs, in order to research the substitution between labor and other inputs in response to human heat stress.

# Contents
## \in
This folder contains the data (GRIDDATA.har), parameters (GRIDPARM.har) and scope (GRIDSETS.har) of SIMPLE-G.
## \out
This folder will contain results after simulation.
## \cmf_HeatStress_baseline
This folder contains the command files (*.cmf), which specify the experiment to be simulated. Here we only conduct simulations with the impact of human heat stress on labor productivity under each GCM projection at the 2010 baseline. 
## \cmf_HeatStress_2050
This folder contains the command files that include not only the impact of human heat stress on labor productivity, but also the projection of changes on socio-economic development (population, per capita GDP, technology, biofuel), crop yield and groundwater extractions during 2010 - 2050.
## \shf
This folder contains the shock files of projected labor productivity loss due to human heat stress for the US (grid cell level) and non-US regions (regional level), which are called in command files.
## SIMPLEG_IGS.tab
The source code of model. The simulation with SIMPLE-G requires the General Equilibrium Modelling PACKage (GEMPACK) software.
## SIMPLEG_IGS.exe
This is the compiled exe version of the SIMPLE-G model.
## run.bat
This batch file execuates simulations with command files. 
## run.bat
Auxiliary files for simulation (no need to change or edit them).

# How to conduct simulations
## Step 1: Install GEMPACK
Please install GEMPACK (release 12) (https://www.copsmodels.com/gpver.htm) on user's computer with Window platform (We have tested the model with Win10 / Win11 OS, the install time should be less than 5 minutes). It is necessary to obtain a license of GEMPACK in order to run simulations. A limited-time free-trial license is available from https://www.copsmodels.com/gpeidl.htm. 

## Step 2: Select command files
Please copy and paste the command files (*.cmf) to be simulated from the corresponding "cmf_" folder to the SIMPLEG-US_HeatStress folder (in the same folder with SIMPLEG_IGS.exe and run.bat)

## Step 3: Modify command files and the batch file (optional)
You may use the default "run.bat" file to replicate our results. Alternatively, you may make changes on the cmf files, and then open "run.bat" with any text editor (for example notepad) and only keep lines with the cmf files to be simulated before the "pause" line, then save the file (The simulation of each cmf file will take around 20 - 40 minutes, depending on user's computer).

## Step 4: Conduct simulations
Please double click "run.bat", it will automatically run all simulations identified and save results to "out" folder.

## Step 5: View and analyze results
Results (*.sl4 files in the "out" folder) can be viewed with the ViewSOL software (installed together with GEMPACK). You can also analyze results with the code available from https://github.com/wangzhan90/HeatStressPaper_result.
