##About source data

As sourse data for work was used Human Activity Recognition Using Smartphones Data Set. A full description is available at the site where the data was obtained: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones Here are the data for the project: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

##About R script

File with R code "run_analysis.R" perform 5 following steps (in accordance assigned task of course work):
###1. Merges the training and the test sets to create one data set.
 #### 1.1 Read files 
  ####1.1.1 subject_train.txt,X_train.txt and y_train.txt read these trainings data files
 #### 1.1.2 subject_test.txt,X_test.txt and y_test.txt these testing data files
  ####1.1.3 features.txt contains information of all variables in training and testing data sets.Read it and store it
  ####1.1.4 activity_lables provides activity names for the lables used.Read it and store it.
  ####1.2 Using features data read assign column names to training and testing data sets.
  ####1.3 Since training and testing data sets follow same structure we can merge them by 
       a) first column binding(subject_train.txt,X_train.txt and y_train.txt) training and 
       (subject_test.txt,X_test.txt and y_test.txt )
       testing data sets with
       b) Then row binding training and testing datasets
###2. Extracting only the measurements on the mean and standard deviation for each measurement
  ####2.1 Read column names from the merged dataset and store them.
  ####2.2 Create vector for defining ID, mean and standard deviation from stored column names
 ####2.3 Using vector created in 2.2 step subset merged dataset to get mean and standard deviation data
###3. Using descriptive activity names to name the activities in the data set
###4. Appropriately labeling the data set with descriptive variable names
###5. Creating a second, independent tidy data set with the average of each variable for each activity and each subject
  ####5.1 Making second tidy data set
  ####5.2 Writing second tidy data set in txt file

The code takes for granted all the data is present in the same folder, un-compressed and without names altered.

##About variables:

x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
x_data, y_data and subject_data merge the previous datasets to further analysis.
features contains the correct names for the x_data dataset, which are applied to the column names stored in
