# Credit is Gold

# Libaries Imported
import numpy as np
import pandas as pd
from pathlib import Path
from sklearn.metrics import balanced_accuracy_score
from sklearn.metrics import confusion_matrix
from imblearn.metrics import classification_report_imbalanced

import warnings
warnings.filterwarnings('ignore')

# Lets give out some $
read in csv file # Read the CSV file from the Resources folder into a Pandas DataFrame
lending_data = pd.read_csv(Path("./lending_data.csv"))

# Review the DataFrame
lending_data

# Machines rule !
seperated the data into two seperate training frames to train the module on for it 
to get use to the data and uderstand what the data was, from their I fit the module
to the algorithim and then used the predict function to get the accuracy score of the module
which was at 94%
![image](https://user-images.githubusercontent.com/106267420/186948655-06c82ba8-a6be-44fe-9c33-72bb96bafe7a.png)


# Oversampling !
Testing the module to see how reliable that 94% was as a majority of the data it tested on was
data that would read back a 0 so I needed to run the oversampling method to make it a fair ball
game aka equal out the data it was receving and re-run the module to test for accuracy. After
module was trained fit and predicted with the from # imblearn.over_sampling import RandomOverSampler
was an accuracy score of 99%.
![image](https://user-images.githubusercontent.com/106267420/186947977-1c09ae6f-d5f7-4911-9a5d-aaf82acc9b53.png)

# MachineslearningisAwesome!
I have confidence this machine module well now help predict healthy and unheathly 
loans for your company and save you cost of defaulting loans. 


# Recall & Precesion Original Vs Oversampled
The Precesion on the original module was better at 100% on healthy loans  compared to 99% on the oversampled, but I wanted
to test the unhealthy loans and make sure that was more closer accurate. Oversampled showed 99% compared to 85% from the original 
module. 
