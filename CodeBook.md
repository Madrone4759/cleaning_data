-- ASSUMPTIONS --

If you want to download the dataset before running the script, ensure the UCI HAR Dataset folder is in your working directory in a folder called "acc_data". The files will be saved into the UCI HAR Dataset folder in this directory. If this does not exist when the script is run, the directory will be created and the file will be downloaded.


-- SCRIPT DESCRIPTION --

The project.R file performs the following steps to clean and process the UCI HAR dataset:
1. Checks if the data exists in your working directory. If not, then it downloads the zip file and unzips it
2. Assigns column names to the data based on the feature names in the features.txt file
3. Selects only the mean and standard deviation for each feature
4. assigns the activity name based on the activity id and values in the activity_labels.txt file
5. Combines training and test datasets and outputs the combined data to a file called combined_data.txt
6. Calculates the mean of each feature value at the subject and activity level, and outputs that to a file called grouped_data.txt


-- OUTPUT FILE DESCRIPTIONS --
Both files that are ouput from the script have the same columns - the only difference is the grouped dataset has one line per subject and activity, with the mean of each observation for that subject/activity combo. The combined dataset contains all observations.

-- VARIABLES --
Here are the variables that are contained in the files:

subject_id - The unique ID that represents the subject these observations are for
activity_name - the activity the subject was performing when the measurements took place
tBodyAcc_mean_X - Mean of the time domain signal of the body acceleration in the X direction
tBodyAcc_mean_Y - Mean of the time domain signal of the body acceleration in the Y direction
tBodyAcc_mean_Z - Mean of the time domain signal of the body acceleration in the Z direction
tBodyAcc_std_X - Standard Deviation of the time domain signal of the body acceleration in the X direction
tBodyAcc_std_Y - Standard Deviation of the time domain signal of the body acceleration in the Y direction
tBodyAcc_std_Z - Standard Deviation of the time domain signal of the body acceleration in the Z direction
tGravityAcc_mean_X - Mean of the time domain signal of the body gravity in the X direction
tGravityAcc_mean_Y - Mean of the time domain signal of the body gravity in the Y direction
tGravityAcc_mean_Z - Mean of the time domain signal of the body gravity in the Z direction
tGravityAcc_std_X- Standard Deviation  of the time domain signal of the body gravity in the X direction
tGravityAcc_std_Y- Standard Deviation  of the time domain signal of the body gravity in the Y direction
tGravityAcc_std_Z- Standard Deviation  of the time domain signal of the body gravity in the Z direction
tBodyAccJerk_mean_X - Mean of the time domain signal of the body acceleration jerk in the X direction
tBodyAccJerk_mean_Y - Mean of the time domain signal of the body acceleration jerk in the Y direction
tBodyAccJerk_mean_Z - Mean of the time domain signal of the body acceleration jerk in the Z direction
tBodyAccJerk_std_X - Standard Deviation of the time domain signal of the body acceleration jerk in the X direction
tBodyAccJerk_std_Y - Standard Deviation of the time domain signal of the body acceleration jerk in the Y direction
tBodyAccJerk_std_Z - Standard Deviation of the time domain signal of the body acceleration jerk in the Z direction
tBodyGyro_mean_X - Mean of the time domain signal of the body angular velocity in the X direction
tBodyGyro_mean_Y - Mean of the time domain signal of the body angular velocity in the Y direction
tBodyGyro_mean_Z - Mean of the time domain signal of the body angular velocity in the Z direction
tBodyGyro_std_X - Standard Deviation of the time domain signal of the body angular velocity in the X direction
tBodyGyro_std_Y - Standard Deviation of the time domain signal of the body angular velocity in the Y direction
tBodyGyro_std_Z - Standard Deviation of the time domain signal of the body angular velocity in the Z direction
tBodyGyroJerk_mean_X - Mean of the time domain signal of the body angular velocity jerk in the X direction
tBodyGyroJerk_mean_Y - Mean of the time domain signal of the body angular velocity jerk in the Y direction
tBodyGyroJerk_mean_Z - Mean of the time domain signal of the body angular velocity jerk in the Z direction
tBodyGyroJerk_std_X - Standard Deviation of the time domain signal of the body angular velocity jerk in the X direction
tBodyGyroJerk_std_Y - Standard Deviation of the time domain signal of the body angular velocity jerk in the Y direction
tBodyGyroJerk_std_Z - Standard Deviation of the time domain signal of the body angular velocity jerk in the Z direction
tBodyAccMag_mean - Mean of the magnitude of the time domain signal of the three-dimensional body acceleration
tBodyAccMag_std - Standard Deviation of the magnitude of the time domain signal of the three-dimensional body acceleration
tGravityAccMag_mean - Mean of the magnitude of the time domain signal of the three-dimensional body gravity
tGravityAccMag_std - Standard Deviation of the magnitude of the time domain signal of the three-dimensional body gravity
tBodyAccJerkMag_mean - Mean of the magnitude of the time domain signal of the three-dimensional body acceleration jerk
tBodyAccJerkMag_std - Standard Deviation of the magnitude of the time domain signal of the three-dimensional body acceleration jerk
tBodyGyroMag_mean - Mean of the magnitude of the time domain signal of the three-dimensional body angular velocity
tBodyGyroMag_std - Standard Deviation of the magnitude of the time domain signal of the three-dimensional angular velocity
tBodyGyroJerkMag_mean - Mean of the magnitude of the time domain signal of the three-dimensional body angular velocity jerk
tBodyGyroJerkMag_std - Standard Deviation of the magnitude of the time domain signal of the three-dimensional body angular velocity jerk
fBodyAcc_mean_X - Mean of the frequency signal of the body acceleration in the X direction
fBodyAcc_mean_Y - Mean of the frequency signal of the body acceleration in the Y direction
fBodyAcc_mean_Z - Mean of the frequency signal of the body acceleration in the Z direction
fBodyAcc_std_X - Standard Deviation of the frequency signal of the body acceleration in the X direction
fBodyAcc_std_Y - Standard Deviation of the frequency signal of the body acceleration in the Y direction
fBodyAcc_std_Z - Standard Deviation of the frequency signal of the body acceleration in the Z direction
fBodyAccJerk_mean_X - Mean of the frequency signal of the body acceleration jerk in the X direction
fBodyAccJerk_mean_Y - Mean of the frequency signal of the body acceleration jerk in the Y direction
fBodyAccJerk_mean_Z - Mean of the frequency signal of the body acceleration jerk in the Z direction
fBodyAccJerk_std_X - Standard Deviation of the frequency signal of the body acceleration jerk in the X direction
fBodyAccJerk_std_Y - Standard Deviation of the frequency signal of the body acceleration jerk in the Y direction
fBodyAccJerk_std_Z - Standard Deviation of the frequency signal of the body acceleration jerk in the Z direction
fBodyGyro_mean_X - Mean of the frequency signal of the body angular velocity in the X direction
fBodyGyro_mean_Y - Mean of the frequency signal of the body angular velocity in the Y direction
fBodyGyro_mean_Z - Mean of the frequency signal of the body angular velocity in the Z direction
fBodyGyro_std_X - Standard Deviation of the frequency signal of the body angular velocity in the X direction
fBodyGyro_std_Y - Standard Deviation of the frequency signal of the body angular velocity in the X direction
fBodyGyro_std_Z - Standard Deviation of the frequency signal of the body angular velocity in the X direction
fBodyAccMag_mean - Mean of the magnitude of the frequency signal of the three-dimensional body acceleration
fBodyAccMag_std - Standard Deviation of the magnitude of the frequency signal of the three-dimensional body acceleration
fBodyBodyAccJerkMag_mean - Mean of the magnitude of the frequency signal of the three-dimensional body acceleration jerk
fBodyBodyAccJerkMag_std - Standard Deviation of the magnitude of the frequency signal of the three-dimensional body acceleration jerk
fBodyBodyGyroMag_mean - Mean of the magnitude of the frequency signal of the three-dimensional body angular velocity
fBodyBodyGyroMag_std - Standard Deviation of the magnitude of the frequency signal of the three-dimensional body angular velocity
fBodyBodyGyroJerkMag_mean - Mean of the magnitude of the frequency signal of the three-dimensional body angular velocity jerk
fBodyBodyGyroJerkMag_std - Standard Deviation of the magnitude of the frequency signal of the three-dimensional body angular velocity jerk