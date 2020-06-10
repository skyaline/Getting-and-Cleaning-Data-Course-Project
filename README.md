**Getting-and-Cleaning-Data-Course-Project**

Repository for Coursera Data Science Course "Getting and Cleaning Data" Course Project
The aim of this project is to demonstrate the ability to collect, work, and clean up a data set. Data collected from the accelerometers of the Samsung Galaxy S smartphone were used. A full description is here:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Here are the data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

This repository contains:

- R script called `run_analysis.R` that does the following:

1.Merges the training and the test sets to create one data set.
2.Extracts only the measurements on the mean and standard deviation for each measurement.
3.Uses descriptive activity names to name the activities in the data set
4.Appropriately labels the data set with descriptive variable names.
5.From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

- `CodeBook.md` a code book that describes the variables, the data, and any transformations or work that I performed to clean up the data.

- `FinalData.txt` is the file that consists of the average (mean) of each variable for each subject and each activity.
