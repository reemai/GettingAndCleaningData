##Getting and Cleaning Data Assignment
=======================================

How script (run_analysis.R) works
---------------------------------------

* Unzip data in the folder ~/UCI HAR Dataset/ (https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)
* run_analysis.R should be saved in ~/UCI HAR Dataset/
* In RStudio, set the working directory to ~/UCI HAR Dataset
* Use the command source("run_analysis.R") in RStudio
* Two output files are generated
	-merged_clean_data.txt is a data frame called cleaned with a 10299x68 dimension 
	-independent_tidy_data_set_with_averages.txt called result with a 180x68 dimension
* Use the command data <- read.table("independent_tidy_data_set_with_averages.txt") in order to read the data
	-The data is 180x68 since there are 30 subjects and 6 activities and the 180 rows contains all the combinations
	  
