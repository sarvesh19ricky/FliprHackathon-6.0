# FliprHackathon-6.0
Team name Reboot Rebels
Team : Sarvesh S and Sanjay Kumar K
Task 1
How to use- Place all the files which are available in the Task1 folder in the same directory. The order to be followed is:
Each file has locations marked where you need to pass the address to your dataset files. Each of the preprocessing files will output a data file which will be take up by the next file. The final predictions file output a file with the predicted covid cases for each data provided in the test dataset.
The first file takes care of all the features that have missing values, except population [2011], population [2001] and female population. Based of the distribution observed, relevant adjustments were made (mean, mode or other statistical values were used here, see code for further details).
The second preprocessing file makes adjustments for missing population [2011] values (48 in total). Population for 2011, population for 2001 and female population had high correlation, thus only one was to be used, to avoid over-fitting. At the same time, the other two could be used to fill the population 2011 missing values. Using simple linear regression model, we adjusted the values in the dataset.
The last file takes care of adding categorical features in the final data file. We made predictions using a numbers of regressions (Linear, SVR, xgboost, random forest, etc.). Out of these, random forest gave the least error along with minimum spread and maximum score, thus emerging as a clear choice. Same was used for making predictions, and at last the values obtained were saved in a file
