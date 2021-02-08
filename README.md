# gcd_course_project
Getting and Cleaning Data Course Project

Overview

This repository contains the raw data from UCI Machine Learning Repository - Human Activity Recognition Using Smartphones Data Set http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones An R script (run_analysis.R) has been included which takes the raw training and test data files and transforms them into one set of tidy data. The R script generates tidy_data_avg.txt as an output.

The script, run_analysis.R, performs the following steps:
1. Checks if the file and directory already exit. If not, download and create.
2. Merges the training and the test sets to create one data set.
3. Extracts only the measurements on the mean and standard deviation for each measurement.
4. Uses descriptive activity names to name the activities in the data set
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
6. Create output in tidy_data_avg.txt