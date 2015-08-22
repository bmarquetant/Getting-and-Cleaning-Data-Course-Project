==================================================================

PROJECT TITLE: Getting and Cleaning Data Course Project
==================================================================

PROJECT OBJECTIVE

This purpose of this project is to  collect, work with, and clean a raw data set. The goal is to prepare tidy data that can be used for later analysis.
==================================================================

RAW DATA

The source of the raw data if the Human Activity Recognition Using Smartphones Dataset (Version 1.0). 

The raw data represent data collected from the accelerometers from the Samsung Galaxy S smartphone. 

A full description is available at the site where the data was obtained: 

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones#

Link to the database: http://archive.ics.uci.edu/ml/machine-learning-databases/00240/

The following raw data files were used in the analysis:

- 'train/X_train.txt': Training set.

- 'test/X_test.txt': Test set.

- 'train/y_train.txt': Activity codes for training set.

- 'test/y_test.txt': Activity codes for test set.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'subject_train.txt': Each row identifies the subject who performed the activity for each window sample in the training set. Its range is from 1 to 30.

- 'subject_test.txt': Each row identifies the subject who performed the activity for each window sample in the test set. Its range is from 1 to 30.
==================================================================

SCRIPT FOR PERFORMING THE ANALYSIS

## Step 1: loading "dplyr" and "reshape2" R packages 

library(dplyr)
library(reshape2)

## Step 2: reading in the test and training data sets into a dataframe object and merge them to create a combined dataframe with 10299 observations for 561 variables

df.test <- read.table("X_test.txt")
df.train <- read.table("X_train.txt")
df <- rbind(df.test, df.train)

## Step 3: reading in the activity code data sets pertinent to the test and training data sets into a dataframe object and merge them to create a combined dataframe containing activity code for 10299 observations

act.train <- read.table("y_train.txt")
act.test <- read.table("y_test.txt")
act <- rbind(act.train, act.test)

## Step 4: reading in the subject ID data sets pertinent to the test and training data sets into a dataframe object and merge them to create a combined dataframe containing subject IDs for 10299 observations

subject.test <- read.table("subject_test.txt")
subject.train <- read.table("subject_train.txt")
subject <- rbind(subject.test, subject.train)

## Step 5: reading in the table containing the activity codes and corresponding activity labels into a dataframe

act.labels <- read.table("activity_labels.txt")

## Step 6: reading in the table containing feature labels into a dataframe

features <- read.table("features.txt")

## Step 7 :Subsetting the features dataframe (containing 561 features) to contain only measurements on the mean and standard deviation (66 measurements)
## 	   The resulting daraframe called 'featureID' contains the original column numbers and corresponding feature names 

featuresSubsetMean <- features[grep("mean()", features$V2), ]
featuresSubsetMean <- featuresSubsetMean[- grep("Freq", featuresSubsetMean$V2), ]
featuresSubsetStd <- features[grep("std()", features$V2), ]
featureID <- rbind(featuresSubsetMean, featuresSubsetStd)

## Step 8: extract only those columns of the merged dataframe created in step 2 that contain mean and standard deviation measurements

df <- select(df, featureID$V1)

## Step 9: merge dataframe with activity codes created in step 3, dataframe with subject IDs created in step 4, and the dataframe containing mean and standard deviation measurements created in step 8. 

df <- cbind(act, subject, df)

## Step 10: from the 2nd column of the dataframe created in step 7, create a character vector containing descriptive names for the 66 variables

featureDesc <- as.character(featureID$V2)

## Step 11: label the data set created in step 9 with descriptive variable names 

names(df) <- c("ActivityID","Subject ID", featureDesc)

## Step 12: add a new variable to the dataframe created in setp 11 which will contain descriptive activity names to name the activities in the data set. This will be done by looking up the corresponding activity label for each activity code.

df$Activity <- as.character(act.labels[match(df$ActivityID, act.labels$V1), 2])
df$Activity <- as.factor(df$Activity)

## Step 13: from the data set created in step 12, creates a second, independent tidy data set with the average of each variable for each activity and each subject, by first melting and then casting the data frame. 

dfMelt <- melt(df, id=c("Activity","SubjectID"), measure.vars=featureDesc)
data <- dcast(dfMelt, Activity + SubjectID ~ variable, mean)

## Step 14: write the data set created in step 13 into a text file called "tidydata.txt"

write.table(data, "tidydata.txt")

==================================================================

TIDY DATA

The tidy data set (stored in "tidydata.txt" file) contains the average values for the selected 66 mean and standard deviation variables for each activity and subject ID combination (6 activity x 30 subjects = 180 combinations).

