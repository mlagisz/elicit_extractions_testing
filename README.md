Project title: "Using Elicit AI research assistant for data extraction in systematic reviews: a feasibility study across environmental and life sciences""
 
Authors: Malgorzata Lagisz, Ayumi Mizuno#, Kyle Morrison#, Pietro Pollo#,  Lorenzo Ricolfi#, Yefeng Yang#, Shinichi Nakagawa#
 # these authors contributed equally and are listed in alphabetical order
 
Correspondiung author: Malgorzta Lagisz


## Instructions
To reproduce the analyses, please follow these steps:
1. Install R and RStudio on your computer.
2. Download all files and folders from this Repository
3. Execute script "R/analyses.Rmd" will produce numbers and figures in the manuscript


## Repo content   
This repository contains following folders and files:   

- Folder 'R" - contains code for data processing, analyses and figures for the manuscript in the file "analyses.Rmd"

- Folder 'plots" - contains saved figures for the manuscript in .png format (produced by analyses.Rmd code)

- Folder 'data_raw" - contains processed data files used for analyses:
    Sub-folder: "1_TEST_data_raw" which contains all raw data files (CSV) from the TEST phase of Elicit extractions, following naming convention:
                  ReviewCode_TEST_Elicit - VariableName.csv
    Sub-folder: "2_RETEST_data_raw" which contains all raw data files (CSV) from the RETEST phase of Elicit extractions, following naming convention:
                  ReviewCode_RETEST_Elicit - VariableName.csv     
    Sub-folder: "3_HATEST_data_raw" which contains all raw data files (CSV) from the HATEST phase of Elicit extractions, following naming convention:
                  ReviewCode_HATEST_Elicit - VariableName.csv   

- Folder 'data_processed" - contains processed data files (CSV) used for analyses:
      File: "mismatched_NA_values_TEST_HATEST_ML.csv" which contains mismatched and NA extracted raw data between TEST and HATEST in columns Extracted_value_TEST	and Extracted_value_HATEST, with manual annotations for Reason and comments by ML   
      File: "mismatched_NA_values_TEST_HATEST.csv" which contains mismatched and NA extracted raw data between TEST and HATEST in columns Extracted_value_TEST	and Extracted_value_HATEST (as exported from R during data processing)   
      File: "mismatched_NA_values_TEST_RETEST_ML.csv" which contains mismatched and NA extracted raw data between TEST and RETEST in columns Extracted_value_TEST	and Extracted_value_RETEST, with manual annotations for Reason and comments by ML   
      File: "mismatched_NA_values_TEST_RETEST.csv" which contains mismatched and NA extracted raw data between TEST and RETEST in columns Extracted_value_TEST	and Extracted_value_RETEST (as exported from R during data processing)   
      File: "newdata_GS_TEST_merged.csv" which contains merged data from TEST (extracted by Elicit) and GS (gold standard human-extracted), subsetted to compare extraction accuracy for the same set of variables from the main TEST phase in Elicit and human-extractions (double-extracted).
      File: "summary_per_review_DEV.csv" which contains summary of numbers of iterations and extraction accuracy per review across all variables for the DEV (Elicit prompt development) phase
      File: "summary_per_review_TEST.csv" which contains summary of extraction accuracy per review across all variables for the TEST (Elicit first testing) phase
      
- "LICENSE.txt" - licence information for the data and code reuse and attribution

