==================================================================

CODE BOOK

==================================================================

UNITS OF MEASUREMENT OF VARIABLES 

A full description on the methodology of collecting and computing the raw data is available at the site where the data was obtained: 

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones#

Features in the raw data are normalized and bounded within [-1,1].

==================================================================

TRANSFORMATION PERFORMED TO CLEAN UP THE RAW DATA

- Raw data files ("X_train.txt", "X_test.txt", "y_train.txt", "y_test.txt", "subject_train.txt", "subject_test.txt") were merged to create a single data frame.
- The merged dataset was subset for 68 columns:
	- column containing activity code
	- column containing subject IDs
	- 66 columns containing mean and standard deviation features
- Data set has been labelled with descriptive variable names (descriptive feature labels were sourced from 'features.txt' raw data file
- An additional column was added to contain activity labels
- By melting and casting the data set, an independent tidy data set has been created with the average of each 66 variables for each activity and each subject

==================================================================

VARIABLE DICTIONARY

VARIABLE NAME			VARIABLE DESCRIPTION

Activity			The activity performed by the volunteers while wearing a smartphone (Samsung Galaxy S II) on the waist during the experiment (the 6 activities performed are: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING).

SubjectID			The unique identifier of the subject (there were 30 volunteers participating in the experiment) who performed the activity for each window sample.
 
tBodyAcc-mean()-X		The average of the mean values of the body acceleration time domain signals from the smartphone accelerometer X axis for a given activity and a given subject.	
 
tBodyAcc-mean()-Y		The average of the mean values of the body acceleration time domain signals from the smartphone accelerometer Y axis for a given activity and a given subject.	
 
tBodyAcc-mean()-Z		The average of the mean values of the body acceleration time domain signals from the smartphone accelerometer Z axis for a given activity and a given subject.	
 
tGravityAcc-mean()-X		The average of the mean values of the gravity acceleration time domain signals from the smartphone accelerometer X axis for a given activity and a given subject.	
 
tGravityAcc-mean()-Y		The average of the mean values of the gravity acceleration time domain signals from the smartphone accelerometer Y axis for a given activity and a given subject.
 
tGravityAcc-mean()-Z		The average of the mean values of the gravity acceleration time domain signals from the smartphone accelerometer Z axis for a given activity and a given subject.
 
tBodyAccJerk-mean()-X		The average of the mean values of the body acceleration time domain jerk signals from the smartphone accelerometer X axis for a given activity and a given subject.
 
tBodyAccJerk-mean()-Y		The average of the mean values of the body acceleration time domain jerk signals from the smartphone accelerometer Y axis for a given activity and a given subject.
 
tBodyAccJerk-mean()-Z		The average of the mean values of the body acceleration time domain jerk signals from the smartphone accelerometer Z axis for a given activity and a given subject.
 
tBodyGyro-mean()-X		The average of the mean values of the body acceleration time domain signals from the smartphone gyroscope X axis for a given activity and a given subject.
 
tBodyGyro-mean()-Y		The average of the mean values of the body acceleration time domain signals from the smartphone gyroscope Y axis for a given activity and a given subject.
 
tBodyGyro-mean()-Z		The average of the mean values of the body acceleration time domain signals from the smartphone gyroscope Z axis for a given activity and a given subject.
 
tBodyGyroJerk-mean()-X		The average of the mean values of the body acceleration time domain jerk signals from the smartphone gyroscope X axis for a given activity and a given subject.
 
tBodyGyroJerk-mean()-Y		The average of the mean values of the body acceleration time domain jerk signals from the smartphone gyroscope Y axis for a given activity and a given subject.
 
tBodyGyroJerk-mean()-Z		The average of the mean values of the body acceleration time domain jerk signals from the smartphone gyroscope Z axis for a given activity and a given subject.
 
tBodyAccMag-mean()		The average of the mean values of the magnitude of three-dimensional body acceleration time domain signals from the smartphone accelerometer for a given activity and a given subject.
 
tGravityAccMag-mean()		The average of the mean values of the magnitude of three-dimensional gravity acceleration time domain signals from the smartphone accelerometer for a given activity and a given subject.
 
tBodyAccJerkMag-mean()		The average of the mean values of the magnitude of three-dimensional body acceleration time domain jerk signals from the smartphone accelerometer for a given activity and a given subject.
 
tBodyGyroMag-mean()		The average of the mean values of the magnitude of three-dimensional body acceleration time domain signals from the smartphone gyroscope for a given activity and a given subject.
 
tBodyGyroJerkMag-mean()		The average of the mean values of the magnitude of three-dimensional body acceleration time domain jerk signals from the smartphone gyroscope for a given activity and a given subject.
 
fBodyAcc-mean()-X		The average of the mean values of the body acceleration frequency domain signals from the smartphone accelerometer X axis for a given activity and a given subject.		
 
fBodyAcc-mean()-Y		The average of the mean values of the body acceleration frequency domain signals from the smartphone accelerometer Y axis for a given activity and a given subject.
 
fBodyAcc-mean()-Z		The average of the mean values of the body acceleration frequency domain signals from the smartphone accelerometer Z axis for a given activity and a given subject.
 
fBodyAccJerk-mean()-X		The average of the mean values of the body acceleration frequency domain jerk signals from the smartphone accelerometer X axis for a given activity and a given subject.
 
fBodyAccJerk-mean()-Y		The average of the mean values of the body acceleration frequency domain jerk signals from the smartphone accelerometer Y axis for a given activity and a given subject.
 
fBodyAccJerk-mean()-Z		The average of the mean values of the body acceleration frequency domain jerk signals from the smartphone accelerometer Z axis for a given activity and a given subject.
 
fBodyGyro-mean()-X		The average of the mean values of the body acceleration frequency domain signals from the smartphone gyroscope X axis for a given activity and a given subject.
 
fBodyGyro-mean()-Y		The average of the mean values of the body acceleration frequency domain signals from the smartphone gyroscope Y axis for a given activity and a given subject.
 
fBodyGyro-mean()-Z		The average of the mean values of the body acceleration frequency domain signals from the smartphone gyroscope Z axis for a given activity and a given subject.
 
fBodyAccMag-mean()		The average of the mean values of the magnitude of three-dimensional body acceleration frequency domain signals from the smartphone accelerometer for a given activity and a given subject.	
 
fBodyBodyAccJerkMag-mean()	The average of the mean values of the magnitude of three-dimensional body acceleration frequency domain jerk signals from the smartphone accelerometer for a given activity and a given subject.
 
fBodyBodyGyroMag-mean()		The average of the mean values of the magnitude of three-dimensional body acceleration frequency domain signals from the smartphone gyroscope for a given activity and a given subject.
 
fBodyBodyGyroJerkMag-mean()	The average of the mean values of the magnitude of three-dimensional body acceleration frequency domain jerk signals from the smartphone gyroscope for a given activity and a given subject.
 
tBodyAcc-std()-X		The average of the standard deviation values of the body acceleration time domain signals from the smartphone accelerometer X axis for a given activity and a given subject.
 
tBodyAcc-std()-Y		The average of the standard deviation values of the body acceleration time domain signals from the smartphone accelerometer Y axis for a given activity and a given subject.
 	
tBodyAcc-std()-Z		The average of the standard deviation values of the body acceleration time domain signals from the smartphone accelerometer Z axis for a given activity and a given subject.
 
tGravityAcc-std()-X		The average of the standard deviation values of the gravity acceleration time domain signals from the smartphone accelerometer X axis for a given activity and a given subject.
 
tGravityAcc-std()-Y		The average of the standard deviation values of the gravity acceleration time domain signals from the smartphone accelerometer Y axis for a given activity and a given subject.
 
tGravityAcc-std()-Z		The average of the standard deviation values of the gravity acceleration time domain signals from the smartphone accelerometer Z axis for a given activity and a given subject.
 
tBodyAccJerk-std()-X		The average of the standard deviation values of the body acceleration time domain jerk signals from the smartphone accelerometer X axis for a given activity and a given subject.
 
tBodyAccJerk-std()-Y		The average of the standard deviation values of the body acceleration time domain jerk signals from the smartphone accelerometer Y axis for a given activity and a given subject.
 
tBodyAccJerk-std()-Z		The average of the standard deviation values of the body acceleration time domain jerk signals from the smartphone accelerometer Z axis for a given activity and a given subject.
 
tBodyGyro-std()-X		The average of the standard deviation values of the body acceleration time domain signals from the smartphone gyroscope X axis for a given activity and a given subject.
 
tBodyGyro-std()-Y		The average of the standard deviation values of the body acceleration time domain signals from the smartphone gyroscope Y axis for a given activity and a given subject.
 
tBodyGyro-std()-Z		The average of the standard deviation values of the body acceleration time domain signals from the smartphone gyroscope Z axis for a given activity and a given subject.
 
tBodyGyroJerk-std()-X		The average of the standard deviation values of the body acceleration time domain jerk signals from the smartphone gyroscope X axis for a given activity and a given subject.
 
tBodyGyroJerk-std()-Y		The average of the standard deviation values of the body acceleration time domain jerk signals from the smartphone gyroscope Y axis for a given activity and a given subject.
 
tBodyGyroJerk-std()-Z		The average of the standard deviation values of the body acceleration time domain jerk signals from the smartphone gyroscope Z axis for a given activity and a given subject.
 
tBodyAccMag-std()		The average of the standard deviation values of the magnitude of three-dimensional body acceleration time domain signals from the smartphone accelerometer for a given activity and a given subject.
 
tGravityAccMag-std()		The average of the standard deviation values of the magnitude of three-dimensional gravity acceleration time domain signals from the smartphone accelerometer for a given activity and a given subject.
 
tBodyAccJerkMag-std()		The average of the standard deviation values of the magnitude of three-dimensional body acceleration time domain jerk signals from the smartphone accelerometer for a given activity and a given subject.
 
tBodyGyroMag-std()		The average of the standard deviation values of the magnitude of three-dimensional body acceleration time domain signals from the smartphone gyroscope for a given activity and a given subject.
 
tBodyGyroJerkMag-std()		The average of the standard deviation values of the magnitude of three-dimensional body acceleration time domain jerk signals from the smartphone gyroscope for a given activity and a given subject.
 
fBodyAcc-std()-X		The average of the standard deviation values of the body acceleration frequency domain signals from the smartphone accelerometer X axis for a given activity and a given subject.
 
fBodyAcc-std()-Y		The average of the standard deviation values of the body acceleration frequency domain signals from the smartphone accelerometer Y axis for a given activity and a given subject.
 
fBodyAcc-std()-Z		The average of the standard deviation values of the body acceleration frequency domain signals from the smartphone accelerometer Z axis for a given activity and a given subject.
 
fBodyAccJerk-std()-X		The average of the standard deviation values of the body acceleration frequency domain jerk signals from the smartphone accelerometer X axis for a given activity and a given subject.
 
fBodyAccJerk-std()-Y		The average of the standard deviation values of the body acceleration frequency domain jerk signals from the smartphone accelerometer Y axis for a given activity and a given subject.
 
fBodyAccJerk-std()-Z		The average of the standard deviation values of the body acceleration frequency domain jerk signals from the smartphone accelerometer Z axis for a given activity and a given subject.
 
fBodyGyro-std()-X		The average of the standard deviation values of the body acceleration frequency domain signals from the smartphone gyroscope X axis for a given activity and a given subject.
 
fBodyGyro-std()-Y		The average of the standard deviation values of the body acceleration frequency domain signals from the smartphone gyroscope Y axis for a given activity and a given subject.
	 
fBodyGyro-std()-Z		The average of the standard deviation values of the body acceleration frequency domain signals from the smartphone gyroscope Z axis for a given activity and a given subject.
 
fBodyAccMag-std()		The average of the standard deviation values of the magnitude of three-dimensional body acceleration frequency domain signals from the smartphone accelerometer for a given activity and a given subject.
 
fBodyBodyAccJerkMag-std()	The average of the standard deviation values of the magnitude of three-dimensional body acceleration frequency domain jerk signals from the smartphone accelerometer for a given activity and a given subject.
 
fBodyBodyGyroMag-std()		The average of the standard deviation values of the magnitude of three-dimensional body acceleration frequency domain signals from the smartphone gyroscope for a given activity and a given subject.
 
fBodyBodyGyroJerkMag-std()	The average of the standard deviation values of the magnitude of three-dimensional body acceleration frequency domain jerk signals from the smartphone gyroscope for a given activity and a given subject.



NOTE: for additional information on the experiment and the calculation of the above variables please visit the following website: 
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones