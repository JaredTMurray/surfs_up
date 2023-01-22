# Surfs_up
## Analysis Report

## Overview of the statistical analysis:
for the assignment I used Python, Pandas functions and methods, and SQLAlchemy, to filter the date column of the Measurements table in the [hawaii.sqlite](https://github.com/JaredTMurray/surfs_up/blob/main/hawaii.sqlite) database to retrieve all the temperatures for the month of June and December. I then converted those temperatures to a list, create a DataFrame from the list, and generate the summary statistics.There were two deliverables as follows:
 - Deliverable 1: Determine the Summary Statistics for June
 - Deliverable 2: Determine the Summary Statistics for December

## Results:

## Deliverable 1: Summary Statistics for June 
 - I  import the sqlalchemy extract function, from sqlalchemy import extract and import datetime as dt, to perform the a query that filters the Measurement table to retrieve the temperatures for the month of June.
- See file [SurfUp_Challege file](https://github.com/JaredTMurray/surfs_up/blob/main/SurfsUp_Challenge.ipynb)
- To filter the query through the Measurement table to retrieve the temperatures for the month of June, I used the variable start = dt.datetime(2017, 5, 31), started on the last day in May because it is exclued in the date value from June to satrt at the 1st day in June.I then placed the result in the variable results = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date >= start).all()
-  Convert the June temperatures to a list: I used a for loop to go through the iteration till 2017-06-30
-  Create a DataFrame from the list of temperatures for the month of June: I used the variable(df_june) to store the dataframe aand named the columns. Code "df_june = pd.DataFrame(june_dates, columns=['Date','June Temps'])" 
-  To calculate and print out the summary statistics for the June temperature DataFrame, i used df_june.describe(). See image below
  ![](https://github.com/JaredTMurray/surfs_up/blob/main/Del-1.png)

### Deliverable 2: Summary Statistics for December
- See file [SurfUp_Challege file](https://github.com/JaredTMurray/surfs_up/blob/main/SurfsUp_Challenge.ipynb)
- To query that filters the Measurement table to retrieve the temperatures for the month of December was stored in variable resultsDec = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date >= start_Dec).all()
- Convert the December temperatures to a list: I firat created a emmpty list dec_dates =[] and used a for loop and if statement to go through the iteration and break the loop at result =  ('2017-12-31', 0.01)
- Create a DataFrame from the list of temperatures for the month of December. the variable df_dec = pd.DataFrame(dec_dates, columns=['Date','December Temps']) and print the december results through df_dec.head()
- Calculate and print out the summary statistics for the Decemeber temperature DataFrame, I used the the variable df_dec.describe(). See image belo
- ![](https://github.com/JaredTMurray/surfs_up/blob/main/Del-2.png)

### Summary:
Based on the calculate summary statistics for the June and December temperature, June had a much higher temperture that December.While for min, 25% they both have a recording of 0.0000 while for the 50% SD June0.000000 while December had  0.010000.
