# Getting-and-Cleaning-Data-CourseProject
Repo for Getting and Cleaning Data course project

Run_Analysis.R is R-script to create a tidy dataset for Human Activity Recognition Using Smartphones Dataset
# Input Datasets
features.txt (List of all features)
activity_labels.txt (List of class labels and their activity name)
train/X_train.txt (Training data)
train/y_train.txt (Training labels)
train/subject_train.txt (ID's of subjects in the training data)
test/X_test.txt (Test data)
test/y_test.txt (Test labels)
test/subject_test.txt (ID's of subjects in the training data)

# About run_analysis.R program
The run_analysis.R script merges data from a number of .txt files and produces a tidy data set which may be used for further analysis.
1) First it reads all required .txt files and labels the datasets
2) Then it reads the appropriate "activity_id"'s and "subject_id"'s  and they are appended to the "test" and the "training" data.
3) Then the "test" and "training" data are combined into one single data frame
4) Using the "grep" function, all the columns with mean() and std() values are extracted and then a new data frame is created
5) Using the "merge" function, descriptive activity names are merged with the mean/std values dataset, to get one dataset with descriptive activity names
6) Then with the help of the "melt" and "dcast" functions of the "reshape2" package, the data is converted into a table containing mean values of all the included features, ordered by the activity name and the subject id, and the data is written to the "tidy.txt" file.

Description of the "tidy.txt" file is available in "CodeBook.md". 


# Acknolwedgements:
Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012
