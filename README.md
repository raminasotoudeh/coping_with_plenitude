# Coping with Plenitude:  A Computational Approach to Selecting the Right Algorithm 

## DISCLAIMER: This github page is still a work in progress. It will be updated regularly as I work to clean and prepare the code ahead of publication.

Here, you can find the code and data for the paper, "Coping with Plenitude:  A Computational Approach to Selecting the Right Algorithm", by Sotoudeh and DiMaggio, forthcoming in SMR. All of the analyses were performed in R. The data come from publically available data sets, including the General Social Survey (https://gss.norc.org/) and the American National Election Survey (https://electionstudies.org/). The core functions are described and included in the file, functions.R. The code for running the grid-search simulations is included in simulations.R. The main analyses of the grid-search results is in gridsearch_results.R. Analyses of and predictions for the empirical data can be found in empirical_analyses.R. Finally, the validation analyses are in the script validation.R. Certain scripts are dependent on the results of previous scripts and so below we suggest an order to run them:

1. functions.R
2. simulations.R
3. gridsearch_analyses.R
4. empirical_analyses.R
5. validation.R

Please feel free to direct any questions you may have about the code or paper to sotoudeh@princeton.edu. 
