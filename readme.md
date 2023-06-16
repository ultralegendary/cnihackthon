# CNI hackthon
This repo is a recreation of the datascience task asked in CNI hackthon 2022  
More details on : https://www.cnihackathon.in/

## Problem definition
### Background
- We have a dataset containing information about the buses travelling in Bengaluru. We have obtained it from Bengaluru Metropolitan Transport Corporation (BMTC).
- The region of interest is an approximately 40km by 40km square area. See the following figure:
![BMCT bus tracking](/images/RegionOfInterest.png)
- The data was collected from around two thousand buses for one day, between 7:00am to 7:00pm.
- The buses follow different routes within the city.
- Each bus is identified with a unique ID. A bus carries a device which records the data: latitude, longitude, speed, and timestamp.
### Task
Create a model to estimate the travel time, in minutes, between source-destination pairs using the provided dataset.
### Submission
**Build EstimatedTravelTime() within Predict.py**
```py
"""
This Python code snippet serves two purposes:
1. illustrates how to use relative path
2. provides the template for code submission
ASSUMPTION: 
1. This Python code is present in the folder 'srika_DS_456AB'.
2. BMTC.parquet.gzip, Input.csv, and GroundTruth.csv are present in the folder 'data'
"""
import pandas as pd
# import other packages here
from math import radians, cos, sin, asin, sqrt

"""
ILLUSTRATION: HOW TO USE RELATIVE PATH
Given the above mentioned assumptions, when you run the code, the following three commands will read the files 
containing data, input and, the ground truth.
"""
df = pd.read_parquet('./../data/BMTC.parquet.gzip', engine='pyarrow') # This command loads BMTC data into a dataframe. 
                                                                      # In case of error, install pyarrow using: 
                                                                      # pip install pyarrow
dfInput = pd.read_csv('./../data/Input.csv')
dfGroundTruth = pd.read_csv('./../data/GroundTruth.csv') 
# NOTE: The file GroundTruth.csv is for participants to assess the performance their own codes

"""
CODE SUBMISSION TEMPLATE
1. The submissions should have the function EstimatedTravelTime().
2. Function arguments:
    a. df: It is a pandas dataframe that contains the data from BMTC.parquet.gzip
    b. dfInput: It is a pandas dataframe that contains the input from Input.csv
3. Returns:
    a. dfOutput: It is a pandas dataframe that contains the output
"""
def EstimatedTravelTime(df, dfInput): # The output of this function will be evaluated
    # Function body - Begins
    # Make changes here.
    dfOutput = pd.DataFrame()


    # Function body - Ends
    return dfOutput 
  
"""
Other function definitions here: BEGINS
"""

"""
Other function definitions here: ENDS
"""

dfOutput = EstimatedTravelTime(df, dfInput)
```
