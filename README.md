# Surfs_up
## Analysis Report

## Overview of the statistical analysis:
W. Avy likes wants information about temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round. The Resuslts would content the following:
 - Deliverable 1: Determine the Summary Statistics for June
 - Deliverable 2: Determine the Summary Statistics for December

## Results:

## Deliverable 1: Summary Statistics for June 
 The variable month_june was used to store the June value in the dataframe.

-  A KeyError Traceback (most recent call last)

File ~\anaconda3\lib\site-packages\sqlalchemy\util\_collections.py:186, in Properties.__getattr__(self, key)
    185 try:
--> 186     return self._data[key]
    187 except KeyError:
KeyError: 'measurement'
During handling of the above exception, another exception occurred:
AttributeError                            Traceback (most recent call last)
Input In [42], in <cell line: 9>()
      6 Base.prepare(engine, reflect=True)
      8 # Save references to each table
----> 9 Measurement = Base.classes.measurement
Since I could not determine the excepted results.
[SurfUp_Challege file](#)
### Deliverable 2: Summary Statistics for December
 The variable month_dec was used to store the June value in the dataframe.

You will earn a perfect score for Deliverable 2 by completing all requirements below:
- A working query is written to retrieve the December temperatures from the date column of the Measurement table (10 pt)
- The temperatures are added to a list. (10 pt)
- The list of temperatures is converted to a Pandas DataFrame. (10 pt)
- Summary statistics are generated for the DataFrame. (10 pt)

### Summary:

There is a high-level summary of the results and there are two additional queries to perform to gather more weather data for June and December. (5 pt)
