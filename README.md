# VesselStrikeRiskModel
Vessel strike risk model for large whales


Step 1: Step1_RiskModel.R - runs one loop applying the risk model for the Large (65-350 foot) and OGV (> 350 foot) size classes and a second loop applying the risk model along with the correction factor for the Medium (26-65 foot) size class; outputs bootsrap results as individual CSVs in indivudal size class and year folders

output files: e.g., "ClassL/bootstrap_model_output_2017/whales_boot_L_001_mon01.csv"

Step 2: Step2_Post_RiskModel_Calculate_Mortality.R - organizes bootstrap results into summaries with and without avoidance, calculates mean & sd annual risk over study period, preps data for plotting & manuscript figures

output files: a) e.g., "risk_model_summary_table_L.csv" ; b) e.g., "Avoid_tot_strike_Slow_None_L_2017.csv" ; c) e.g., "No_Avoid_tot_strike_Slow_None_L_2017.csv"

Step 3: Step3_Plot_Mortality.R - creates barplots of mortality for publication; also plots results with and without inclusion of the avoidance parameter 

Step 4: Step4_ProduceMaps.R - Applies risk model to spatial grid and exports results as shapefile; plots risk model results spatially as maps with and without avoidance parameter 
