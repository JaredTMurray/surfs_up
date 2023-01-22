# Surfs_up
## Analysis Report

## Overview of the statistical analysis:
for the assignment I used Python, Pandas functions and methods, and SQLAlchemy, to filter the date column of the Measurements table in the [hawaii.sqlite](https://github.com/JaredTMurray/surfs_up/blob/main/hawaii.sqlite) database to retrieve all the temperatures for the month of June and December. I then converted those temperatures to a list, create a DataFrame from the list, and generate the summary statistics.There were two deliverables as follows:
 - Deliverable 1: Determine the Summary Statistics for June
 - Deliverable 2: Determine the Summary Statistics for December

## Results:

## Deliverable 1: Summary Statistics for June 
 I  import the sqlalchemy extract function, from sqlalchemy import extract and import datetime as dt, to perform the a query that filters the Measurement table to retrieve the temperatures for the month of June.
- See file [SurfUp_Challege file](https://github.com/JaredTMurray/surfs_up/blob/main/SurfsUp_Challenge.ipynb)
- To filter the query through the Measurement table to retrieve the temperatures for the month of June, I used the variable start = dt.datetime(2017, 5, 31), started on the last day in May because it is exclued in the date value from June to satrt at the 1st day in June.I then placed the result in the variable results = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date >= start).all()
-  Convert the June temperatures to a list: 


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
[SurfUp_Challege file](https://github.com/JaredTMurray/surfs_up/blob/main/SurfsUp_Challenge.ipynb)
### Deliverable 2: Summary Statistics for December
 The variable month_dec was used to store the December.
Several errors occur
-  A KeyError Traceback (most recent call last)
-  NameError
-  Attribute Error
See output file [SurfUp_Challege file](https://github.com/JaredTMurray/surfs_up/blob/main/SurfsUp_Challenge.ipynb)

### Summary:
Additional time is needed to add two additional queries to perform to gather more weather data for June and December.
