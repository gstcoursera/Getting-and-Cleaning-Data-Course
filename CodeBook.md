CodeBook
=================================================

This codebook describes the variables, the data, and any transformations or work that I performed to clean up the data 

Site Information: [UC Irvine ML Repo](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

Data: [Download File from UC Irvice ML Repo](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

The code script run_analysis.R performs the following:   

1. Get the data from the source.
2. Read the train data files: *X_train.txt*, *y_train.txt*, *subject_train.txt* and store to appropriate variables.
3. Read the test data files: *X_test.txt*, *y_test.txt*, *subject_test.txt* and store to appropriate variables.
4. Join train and test data to new variables: *data*, *labels*, *subjects*
5. Read the features data file: *features.txt* and store to appropriate variable.
6. Get only the mean and standard deviation values and store to variable: *measurements*
7. Get only the new data using *measurements* and store again to variable: *data*
8. Clean up column names from values as: *()* and *-*
9. Read the activity labels file: *activity_labels.txt* and store to appropriate variable.
10. Clean up column names from value *_* and set all to lower case.
11. Merge data back to *labels*
12. Set appropriate column names to *subjects* and *labels* as: *subject* and *activity*
13. Combine *subjects*, *labels* and *data* to new variable: *combined*
14. Load the required library *reshape2*
15. Melt data using *combined* and by *subject* and *activity* to variable: *newData*
16. Create the new final dataset: *tidyData*
17. Export *tidyData* dataset to file: *tidyData.txt* (removed quotes from column names)
