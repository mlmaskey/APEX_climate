# <p align="center"> APEX_climate </p>
# Climate scenario analysis in agricultural management
## General 
This repository is devoted to analyzing the impact of agricultural management activities on small-scale watersheds under different climate scenarios. The agrohydrological APEX_garze has been used in this study. The agrohydrological model, APEX is Agricultural Policy Environmental eXtender.

Two Python scripts have been made to read different climate data from global circulation models or elsewhere: `pyAPEX` and `run_APEX.` This module uses previously calibrated parameter sets and currently focuses on `APEXgraze` model a variant of APEX with grazing module. 

Following is the comand Line syntax used in terminal:

`python run_APEX.py --type=Scenario --case_id=1 --winepath='' --scen_name=BASE`

* `type`: type of analysis, for instance, scenario analysis
* `case_id`: Parameters based on prescribed perfoemance metrics from calibration. By default, it is 1 for `Objective function value based`
* `winepath`: This is operational parameter, which looks if the mode of computation is Linux or Windows. If it is Windows, just us `'',` otherwise give the path of container
* `scen_name`: Scenario name based on climate model data base

## Steps
1. Make a project folder, e.g., **MyProjec**
2. Compile all the weather data from different climate models or sources under **CLIMATE.**
3. Copy pyAPEX folder build for specific project under the Prpject folder.
4. Make sure **Program** folder under `pyAPEX` has already set up for calibration. The **Program** folder should inherent from the calibrated folder containing all the databases and executible file.
5. Make sure folders: `Utility,` and `Output.` The Output folder contains two files: APEX Parameters obtained from calibration and also relevent statistics.
6. Configure your environment and run in terminal as mentioned before. For commandline interface, it is advised to use `Anaconda command prompt.`

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

  ## Output
  It gnerates two output folders under the project folder: **1) Output_[scen_name]** and **2) Program_[scen_name].** Post analysis should concentrated on the former folder.
  * In the folder with `Output_[scen_name],`  the progrqm genertes atmost 14 files. The most importnt files are `annual.csv`, `daily_basin.csv`, and `daily_outlet.csv` in addition one generic and overqll output file `###RUN.OUT,` where `###RUN` is the name of run
  * **The `annual.csv`** includes selected response varaible at annual scale, e.g., `[YR, CPNM, YLDG, YLDF, BIOM, WS, NS, PS, TS, AS, SS]`
  * **The `daily_basin.csv`** includes selected response varaible at daily scale over the basin, e.g., `[Date, Y, M, D, CPNM, LAI, BIOM, STL, STD, STDL, PRCP, WYLD, TMX, TMN, PET, ET, Q, CN, SSF, PRK, QDR, IRGA, USLE, MUSL, REMX, MUSS, MUST, RUS2, RUSL, YN, YP, QN, QP, QDRN, QPRP, SSFN, RSFN, QRFN, QRFP, QDRP, DPRK, TN, TP]`
  * **The `daily_outlet.csv`** includes selected response varaible at daily scale at the outlet of basin, e.g., `[Date, Y, M, D, RFV, WYLD, TMX, TMN, PET, Q, CN, SSF, PRK, IRGA, USLE, MUSL, REMX, MUSS, MUST, RUS2, RUSL, YSD]`

For description of these variables please refer to: _Osorio J, Zilverberg C, Steglich E, Williams JR (2018) Agricultural Policy/Environmental eXtender Model User’s Manual: Version APEXgraze Rel.1811. Blackland Research and Extension Center_



 
