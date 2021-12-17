# surfs_up
Analysis using SQLite, SQLAlchemy, and Flask

## Analysis Overview:
We were tasked with analyzing a weather dataset taken from weather stations on the island of Oahu to determine if this would be the ideal location to open a surf & shake shop, serving surf boards and ice cream to tourists and locals looking to "hang ten" and cool off with a frozen treat. After first analyzing and reporting on all of the temperature and precipitation data accumulated over multiple years, we were then tasked with two additional deliverables, whick reported on temperature statistics for the months of June and December in the same time period.

## Results: 
We received the following temperature statistics for the months of June and December after completing our analysis:

![June Temps](https://github.com/jmueller187/surfs_up/blob/main/Resources/JuneTempsSummaryStatistics.png)

![December Temps](https://github.com/jmueller187/surfs_up/blob/main/Resources/DecemberTempsSummaryStatistics.png)

We were able to see the following three major points from these results:
1. The average temperatures for June and December only vaired by three degrees, with June's average being 75 degrees and December's average being 71 degrees.
2. The temperatures for June varied by 21 degrees, with a minimum temperature of 64 degrees and a maximum temperature of 85 degrees.
3. The temperatures for December varied over a larger range (27 degrees) with a minimum temperature of 56 degrees and a maximum temperature of 83 degrees.

## Summary: 
From our two temperature deliverables, we can see that the surf and ice cream shop is a business that would be sustainable throughout the entire year. Based on our data, temperatures remain fairly consistent from June to December, which would contribute to a steady flow of customers from the summer months into the winter months.

In addition to temperatures, our dataset also included precipitation data. We could also perform the following two queries to gather precipitation data for the months of June and December.

### Query #1 - gather June precipitation data:
~~~
# Convert the June precipitation to a list.
june_precip_list = [temp.prcp for temp in june_dates]

# Create a DataFrame from the list of precipitaiton for the month of June. 
june_precip_df = pd.DataFrame(june_precip_list, columns=['June Precipitation'])

# Calculate and print out the summary statistics for the June precipitation DataFrame.
june_precip_df.describe()
~~~
Query #1 summary statistics:

![June Precipitation](https://github.com/jmueller187/surfs_up/blob/main/Resources/JunePrecipitationSummaryStatistics.png)

### Query #2 - gather December precipiation data:
~~~
# Convert the December precipitation to a list.
december_precip_list = [temp.prcp for temp in december_dates]

# Create a DataFrame from the list of precipitaiton for the month of December. 
december_precip_df = pd.DataFrame(december_precip_list, columns=['December Precipitation'])

# Calculate and print out the summary statistics for the December precipitation DataFrame.
december_precip_df.describe()
~~~
Query #1 summary statistics:

![December Precipitation](https://github.com/jmueller187/surfs_up/blob/main/Resources/DecemberPrecipitationSummaryStatistics.png)
