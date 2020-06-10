The `run_analysis.R` script performs data preparation and follows the necessary steps, as described in the definition of the course project.

1. **Download the dataset**
   - Dataset downloaded and extracted under the folder called `UCI HAR Dataset`

2. **Assign each data to variables**
   - `features` <- `features.txt` : the features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ.
   - `activities` <- `activity_labels.txt` : list of activities performed when the corresponding measurements were taken and its codes (labels)
   - `subject_test` <- `test/subject_test.txt` : contains test data of 9/30 volunteer test subjects being observed
   - `x_test` <- `test/X_test.txt` : contains recorded features test data
   - `y_test` <- `test/y_test.txt` : contains test data of activities’code labels
   - `subject_train` <- `test/subject_train.txt` : contains train data of 21/30 volunteer subjects being observed
   - `x_train` <- `test/X_train.txt` : contains recorded features train data
   - `y_train` <- `test/y_train.txt` : contains train data of activities’code labels

3. **Merges the training and the test sets to create one data set**
   - `X` is created by merging `x_test` and `x_train` using **rbind()** function
   - `Y` is created by merging `y_test` and `y_train` using **rbind()** function
   - `Subject`is created by merging `subject_test` and `subject_train` using **rbind()** function
   - `Merged_Data` is created by merging `X`, `Y` and `Subject`using **cbind()** function

4. **Extracts only the measurements on the mean and standard deviation for each measurement**
   - `TidyData` is created by subsetting `Merged_Data`, selecting only columns: `subject`, `code` and the measurements on the `mean` and standard deviation (`std`) for each measurement

5. **Uses descriptive activity names to name the activities in the data set**
   - Entire numbers in code column of the `TidyData` replaced with corresponding activity taken from second column of the `activities` variable

6. **Appropriately labels the data set with descriptive variable names**
   - `code` column in `TidyData` renamed into `activities`
   - All `Acc` in column’s name replaced by `Accelerometer`
   - All `Gyro` in column’s name replaced by `Gyroscope`
   - All `BodyBody` in column’s name replaced by `Body`
   - All `Mag` in column’s name replaced by `Magnitude`
   - All start with character `f` in column’s name replaced by `Frequency`
   - All start with character `t` in column’s name replaced by `Time`

7. **From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject**
   - `FinalData` is created by sumarizing `TidyData` taking the means of each variable for each activity and each subject, after groupped by subject and activity.
  - Export `FinalData` into `FinalData.txt file`.
