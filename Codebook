# Code Book

This code book describes variables, data, and any transformations or work performed to clean up the data. These efforts
resulted into a clean and tidy dataset.

# Data Source Details
Original data : https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
Author provided information: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

# Dataset Description

Full details and explanations can be found in 'README.txt' in the ZIP file containing the original data source.

# Quick facts

-> The experiments involved a group of 30 volunteers (19 - 48 years of age)
-> Each person performed six activities while wearing a smartphone (Samsung Galaxy S II) on their waist
-> The activities consisted of three types of walking (flat, upstairs and downstairs), sitting, standing and laying.

# Data Partitioning

The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating 
the training data and 30% the test data.

# Measurements

The following sensor signals were captured using the smartphone's embedded accelerometer and gyroscope:

-> three-axial linear acceleration
-> three-axial angular velocity at a constant rate of 50Hz

The captured signals were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec 
and 50% overlap (128 readings/window). From each window, a vector of features was obtained by calculating variables from the 
time and frequency domain. 

# Transformations

As stipulated by the requirements the following transformations were made to keep the resulting output clean and tidy:

-> The training and the test sets have been merged to form a single data set
-> Out of the broad spectrum of features only the measurements on the mean and standard deviation were considered
-> Descriptive activity names and labels were used appropriately to increase data readability
-> A separate tidy dataset was created as the final step of data refinement efforts
-> In addition to the aforementioned mandatory transformations, the feature names have been amended to adhere to naming standards of the R language. That allowed for an elegant use of R languague features, such as column name filtering, and an increased code readability. I consider this additional transformation a minor change, which I believe doesn't have an adverse impact on the original information.

Feature name adjustment example:

'tBodyAcc-mean()-X' has been changed to 'tBodyAcc_mean_X';
'tBodyAcc-std()-Z' has been changed to 'tBodyAcc_std_Z';
etc.
The transformations are achieved by the script called run_analysis.R, which:

1] Ensures that all non-standard R packages (dplyr, reshape2) are installed
2] Defines a number of helper functions to promote code reuse
3] Downloads the original dataset and verifies its content
4] Loads activity and label names datasets
5] Loads training and test datasets and enhances column names with appropriate labels
6] Merges the testing and the test datasets using dplyr's support for method chaining (pipe operator)
7] Creates an independent tidy dataset based on mean and standard deviations
8] Saves the tidy dataset as tidy_data.txt and tidy_data.csv so that it can be easily imported and viewed
