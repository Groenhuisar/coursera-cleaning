coursera-cleaning
=================

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

calculating the mean of the "mean" and "std" variables

Starting with the original data as mentioned above. In the R script I did the following:

1. read in the files that are needed (test, training, activity and subject of the training/test and the feature-names)

2. Merge the training and test sets (without the activity and subject)

3. Merge the heading to the train/test dat in 2

4. select the variables which include "mean()" or "std()" in the name

5. merge the activity files(test/train) and merge the subject files (test/train)

5. add the columns of activity and subject to the total dataset of point 4

6. change the numbers of the activity to the names of the activity

7. make a new dataframe calculation the mean of the columns of a activiyt/subject combination. 
There are 30 subjects and 6 activity, so in total there are 180 rows with the mean.


Code book:

Activity: Activity of the test people (like walking, sitting, walking_upstairs)

Subject: number (1:30) of a test person (so there are 30 volunteers)

variables:

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

tBodyAcc-XYZ

tGravityAcc-XYZ

tBodyAccJerk-XYZ

tBodyGyro-XYZ

tBodyGyroJerk-XYZ

tBodyAccMag

tGravityAccMag

tBodyAccJerkMag

tBodyGyroMag

tBodyGyroJerkMag

fBodyAcc-XYZ

fBodyAccJerk-XYZ

fBodyGyro-XYZ

fBodyAccMag

fBodyAccJerkMag

fBodyGyroMag

fBodyGyroJerkMag


The set of variables that were estimated from these signals are: 

mean(): Mean value

std(): Standard deviation


