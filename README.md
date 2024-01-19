The project.R script will download and perform a transformation on the UCI HAR dataset, to output two usable files that combines the test and train data, as well as joins supplemental files so you can see the variable names and values, subject id, and activity names all in one file.

The script is designed to be run on MacOS. It can be run as a standalone file, and will even download and unzip the data files into your working directory, so no other prep is needed to run it. It uses all built-in R packages, except for dplyr, which the script will install and load. 

To perform analysis on the data, you should use the combined_data.txt file. This has all the individual observations in separate rows

To view a high level overview of the data, you should use the grouped_data.txt file. This averages each variable at the subject and activity level, so you can see the mean values for each subject and activity.

For more information on the data and how it was collected, visit the data website: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
