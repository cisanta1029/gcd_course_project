# gcd_course_project
Getting and Cleaning Data Course Project

Download the dataset
Dataset downloaded and extracted under the folder called UCI HAR Dataset

Merges the training and the test sets to create one data set.
features <- features.txt : 561 rows, 2 columns
subject_test <- test/subject_test.txt : 2947 rows, 1 column
x_test <- test/X_test.txt : 2947 rows, 561 columns
y_test <- test/y_test.txt : 2947 rows, 1 columns
subject_train <- test/subject_train.txt : 7352 rows, 1 column
x_train <- test/X_train.txt : 7352 rows, 561 columns
y_train <- test/y_train.txt : 7352 rows, 1 columns
x_data (10299 rows, 561 columns) is created by merging x_train and x_test using rbind() function
y_data (10299 rows, 1 column) is created by merging y_train and y_test using rbind() function
subject_data (10299 rows, 1 column) is created by merging subject_train and subject_test using rbind() function
merged_data (10299 rows, 563 column) is created by merging subject_data, x_data and y_data using cbind() function

# Extracts only the measurements on the mean and standard deviation for each measurement.
tidy_data (10299 rows, 88 columns) is created by subsetting Merged_Data, selecting only columns: subject, code and the measurements on the mean and standard deviation (std) for each measurement

# Uses descriptive activity names to name the activities in the data set
activities <- activity_labels.txt : 6 rows, 2 columns

# Appropriately labels the data set with descriptive variable names
code column in TidyData renamed into activities
All Acc in column’s name replaced by Accelerometer
All Gyro in column’s name replaced by Gyroscope
All BodyBody in column’s name replaced by Body
All Mag in column’s name replaced by Magnitude
All start with character f in column’s name replaced by Frequency
All start with character t in column’s name replaced by Time

# From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject
tidy_data_avg (180 rows, 88 columns) is created by sumarizing tidy_data taking the means of each variable for each activity and each subject, after groupped by subject and activity.
Export tidy_data_avg into tidy_data_avg.txt file