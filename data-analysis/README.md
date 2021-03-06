This directory contains all of the descriptive analyses of primary episodes. Both .Rmd files contain one or both of save_output_figs and save_output_tables variables. Changing these to TRUE will save (overwrite) figures and tables in the main CMV-Primary-Infection/figures/ and CMV-Primary-Infection/tables/ directories. These objects, as they appear in the repo, were used in the manuscript or supplement.

A) primary_episode_analysis.Rmd - This code will recreate the analysis and results. Corresponding pdf report walks through it. A lot of the code is organizational for making figures and tables. The quantitative code is mostly in the following script:
  - functions/primary_episode_functions.R: This scripts contains functions that perform the following tasks:
     1. separation of episode into phases for analysis for each infant
     2. linear regression for each phases 
     3. the cubic regression of the clearance phase
     4. the bootstrapping code for correlations
     5. some processing functions so the results look better in tables
     6. validation functions that overlay regression prediction lines over the raw data (use of these functions do not appear in primary_episode_analysis.Rmd)
  - It should be noted that the original names of phases were growth, middle, and decay which correspond to expansion, transition, and clearance in the manuscript, respectively.

B) extended_data_analysis.Rmd - This code and report (pdf) show some additional time series data not presented in the manuscript. It also contains more information on the adjustment of infection times to match oral episode onset and presents the excluded infant data; both of these are briefly discussed in the manuscript.

C) results-data/ directory contains raw data generated by the results analysis in primary_episode_analysis.Rmd
  1. bootstrap spearman correlation results both with and without the two older infants.
  2. results of regression to see if momhiv predicts episode features of age of infection
  3. demo_features_data.csv shows descriptive stats for each infant and phase characteristics
  4. phase_regression_results.csv shows the linear regression results for each phase with 95% confidence intervals for slopes. 
