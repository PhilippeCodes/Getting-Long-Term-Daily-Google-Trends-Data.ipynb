# Getting-Long-Term-Daily-Google-Trends-Data.ipynb
This is a simple template to generate a dataframe or csv with daily google trends data (gtrends) for periods of times that are longer than 90 days.
If you come accross this repository, you probably know that google does not let you retrieve daily trends data for a longer timeframe.
For periods that are longer than 90 days google trends automatically samples the data to a weekly resolution.
Adding insult to injury, the traffic data is relative for each timeframe so that the day at which that highest traffic occured (within the specified period)
is given a value of 100. As a result, we cannot simply stich the the 90 day periods together in order to abtain a longer timeframe of daily traffic data.
Due to the relative nature of the data for each period we have to adjust the values accordingly.

### How To Use:

Simply specifiy your desired parameters on the top and run the whole script.
You will generate a full dataframe with the adjusted daily vaules for the full timeframe and this data will be saves as a csv 'daily_gtrends.csv' in your folder.

Should you have any questions or suggetions, do not hesitate to contact me!
