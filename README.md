# Getting-Long-Term-Daily-Google-Trends-Data.ipynb
This is a simple template to generate a dataframe or csv with daily google trends data (gtrends) for periods of times that are longer than 90 days.   

If you come across this repository, you probably know that Google does not let you retrieve daily trends data for periods that are longer than 90 days otherwise Google trends automatically samples the data to a weekly resolution. Adding insult to injury, the traffic data is relative for each timeframe so that the day at which that highest traffic occurred (within the specified period) is given a value of 100. As a result, we cannot simply stitch the 90 day periods together in order to obtain a longer timeframe of daily traffic data. Due to the relative nature of the data for each period we have to adjust the values for each time period according to a factor which we obtain by looking at the overlapping values.
We compute this factor by dividing the last value of one time period by the first value of the following time period.

### Limitations:

As mentioned, pytrends returns values between 0-100 and we adjust each period by looking at the overlapping dates of each 90-day timeframe. if either one of the overlapping values is 0 the resulting factor is not valid. Should both values be 0, we set the factor to 1 and should only one of the values be 0 we set this value to 0.5 in order to compute the factor.


### How To Use:

Simply specify your desired parameters on the top and run the whole script. You will generate a full dataframe with the adjusted daily values for the full timeframe and this data will be saved as a csv 'daily_gtrends.csv' in your folder.

Should you have any questions or suggestions, do not hesitate to contact me!
