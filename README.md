# surfs_up
Analysis using SQLite, SQLAlchemy, and Flask

## Analysis Overview: Explain the purpose of this analysis.

## Results: Provide a bulleted list with three major points from the two analysis deliverables. Use images as support where needed.

## Summary: Provide a high-level summary of the results and two additional queries that you would perform to gather more weather data for June and December.

### Additional query #1 to gather more weather data:
~~~
# Convert the June precipitation to a list.
june_precip_list = [temp.prcp for temp in june_dates]

# Create a DataFrame from the list of precipitaiton for the month of June. 
june_precip_df = pd.DataFrame(june_precip_list, columns=['June Precipitation'])

# Calculate and print out the summary statistics for the June precipitation DataFrame.
june_precip_df.describe()
~~~

### Additional query #2 to gather more weather data:
~~~
# Convert the December precipitation to a list.
december_precip_list = [temp.prcp for temp in december_dates]

# Create a DataFrame from the list of precipitaiton for the month of December. 
december_precip_df = pd.DataFrame(december_precip_list, columns=['December Precipitation'])

# Calculate and print out the summary statistics for the December precipitation DataFrame.
december_precip_df.describe()
~~~
