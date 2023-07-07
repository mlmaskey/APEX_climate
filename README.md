# APEX_climate : Climate scenario analysis in agricultural management
## General 
This repository is devoted to analyzing the impact of agricultural management activities on small-scale watersheds under different climate scenarios. The agrohydrological APEX_garze has been used in this study. The agrohydrological model, APEX is Agricultural Policy Environmental eXtender.

Two Python scripts have been made to read different climate data from global circulation models or elsewhere: `pyAPEX` and `run_APEX.` This module uses previously calibrated parameter sets and currently focuses on `APEXgraze` model a variant of APEX with grazing module. 

Following is the comand Line syntax used in terminal:

`-----------------------------------------------------------------------------`

`python run_APEX.py --type=Scenario --case_id=1 --winepath='' --scen_name=BASE`

`-----------------------------------------------------------------------------`

* `type`: type of analysis, for instance, scenario analysis
* `case_id`: Parameters based on prescribed perfoemance metrics from calibration. By default, it is 1 for `Objective function value based`
* `winepath`: This is operational parameter, which looks if the mode of computation is Linux or Windows. If it is Windows, just us `'',` otherwise give the path of container
* `scen_name`: Scenario name based on climate model data base

## Steps
1. Make a project folder, e.g., 'MyProjct`
2. Copy pyAPEX folder build for specific project under 'MyProjct` folder
3. Make sure Program folder under `pyAPEX` has already set up for calibration
4. Make sure folders: `Utility,` and `Output.` The Output folder contains two files: APEX Parameters obtained from calibration and also relevent statistics
5. Configure your environment and run in terminal as mentioned before

##  Python dependencies 
* argparse
* os
* shutil
* subproccess
* datetime
* fortranformat
* numpy
* pandas
* others from Utility folder

  

   
  
