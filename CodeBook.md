##Getting and Cleaning Data Assignment
========================================

CodeBook
----------------------------------------

Site where source data was obtained: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
Data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

R script (run_analysis.R) cleans the data with the following steps:

* Merges training and test data sets to create one data set (train/X_train.txt with test/X_test.txt), resulting in a data frame of 10299x561 ("Number of Instances: 10299" and "Number of Attributes: 561")...train/subject_train.txt with test/subject_test.txt, resulting in data frame of 10299x1 (subject IDs)...train/y_train.txt with test/y_test.txt, resulting in a data frame of 10299x1 (activity IDs)
* Reads features.txt and extracts only measuresurements on the mean and standard deviation for each, resulting in a 10299x66 data frame since 66 of the 561 attributes are measurements on the mean and standard deviation.  Measurements seem to be floating point numbers in the range (-1,1).
* Reads activity_labels.txt and applies the descriptive activity names to those in the data set:
	-walking
	-walkingupstairs
	-walkingdownstairs
	-sitting
	-standing
	-laying

* Descriptive names are applied to the data set, merging the 10299x68 data frame with the 10299x1 data frame (contains activity labels and subject IDs), resulting in merged_clean_data.txt (10299x68 data frame: first column has subject IDs, second column has activity names, 66 columns have measurements; subject IDs composed of integers between 1 and 30).
* Attributes are like: tbodyacc-mean-x, tbodyacc-mean-y, tbodyacc-mean-z, tbodyacc-std-x, tbodyacc-std-y, tbodyacc-std-z, tgravityacc-mean-x, tgravityacc-mean-y, tgravityacc-mean-z

* Second file resulting from script is independent_tidy_data_set_with_averages.txt, with the average measurement for each activity and subject, 180x68 data frame (first column has subject IDs, second column has activity names, 66 columns for attributes with averages; included are 30 subjects and 6 activities --> 180 rows in data set with averages)
	
