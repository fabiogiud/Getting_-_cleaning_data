The original files contain datasets related to experiments carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz were captured. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

For each record it is provided:
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

You can find the whole list of variables in the codebook.


STEPS FOR THE ANALYSIS
----------------------
I first uploaded the datasets: test data and training data and then, I read the activity labels and features. Later, I merged the training and test data, creating a new file called "onedataset" (assigning names to the columns). 
Secondly, I extracted the measure of the mean and standard deviation for each measurement and stored them in "data2". Then, I added this new data in "data2" to the merged dataset "onedataset".
Thirdly, I named the activity with the labels.
At point 4, I created a new file called "colnamdata" in order to clean the names of the variables from special characters and make them more readable/understandable. Once I've done this, I added this new labels to the merged dataser "onedataset".
Finally, from this latter dataset I have created the final dataset called "tidy_data" where I calculated the mean for each variable for each activity and each subject using the ddply function from the package plyr. Then, I have exported this dataset as text file.
