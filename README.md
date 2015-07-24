# GetCleanDat
How my script works:

My script comprises the following general 12 points:
1. Setting the working directory and load the libraries.
2. read in the main datasets X_test.txt and X_train.txt.
3. Introduce the column names from features.txt to the datasets test and train.
4. Reduction of the datasets to columns containing the mean and the standard deviation of the respective values.
5. Introduction and tidying of the activity labels.
6. Indroduction of the subject labels to the datasets testlab and trainlab.
7. Introduction of the respective subject and activity labels to the datasets seltest and seltrain, respectively.
8. Combines the datasets seltest and seltrain to a complete dataset containing all test and train measurements.
9. Cleaning up the column names of the final dataset to "tidy names"(removal of special symbols, keep upper case letters only for clarity)
10. Group the resulting dataset final by subject and activity.
11. Summarise the dataset group to receive the mean of evry column in the dataset group for every activity/subject pair.
12. Create the final text file

The datasets test and train are merged to the complete dataset "final" at a very late point in the script (point 8). Before that, they are individually
- read in (point 2)
- labeled with the column names from the features.txt dataset (point 3)
- reduced to the columns containing the mean and std of the respective value (point 4)
- rows are labeled with "tidy" activity and subject names (points 5 - 7)

After merging in point 8, the complete dataset "final" gets "tidy" column names in point 9. With this, the first
four points of the instructions are completed.

The fifth point (creating and independent tidy dataset showing the average values of each activity and each subject)
is completed by subjecting the dataset "final" to the group_by command in point 10 and subjecting the resulting
dataset "group" to the summarise command applying the function "mean" to every group. The resulting dataset "tab" completes
point 5 of the instructions and is written in the text file "NinaDataset.txt", which you will find in this repository.



