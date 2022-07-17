# PyBer_Analysis

## Overview of the analysis

This analysis was conducted to help a fictious CEO of PyBer bettter understand their ride-sharing company better by examining their data. An exploratory analysis was conducted on a dataset containing ride data across three city types (rural, suburban, and urban areas) and a visualization of the results was created.

## Results

### Plan

The analysis consisted of two major components: a data frame that presents an overview of the ride-sharing data by city type, and a line chart visualizing the total fares for each city type.

### Ride-sharing Summary Table

Raw data consisted of two CSV files, one containing driver count information, and other containing ride information. These were combined into one dataframe. This combined dataframe was reorganized and manipulated using the groupby() function with sum() and count() methods in order to ascertain the total drivers, total fares, average fare per ride, and average fare per driver across three city types, rural, suburban, and urban. See [resulting summary dataframe](https://github.com/josephrodini/PyBer_Analysis/blob/main/Resources/ride-sharing_summary.PNG).

We can see several things from this table. There is a trend in which the smaller the city, the fewer the rides and drivers. This makes sense given population density. However, we see the opposite correlation with respect to average fare per ride and average fare per driver: the smaller the city, the higher these figures are. This also makes sense given the relative areas of the three city types.

### Chart of Fares by City Type

Next, data was analyzed in order to determine the weekly fare totals for each city type. Again using the merged dataframe, a new dataframe was created using the pivot() function in order to reset the index and column titles. Then, a dataframe was created to isolate a subset of the ride dates, and the index was again reset. The resample() function and sum() method were then used to get the total fares for each week by city type. See [resulting dataframe](https://github.com/josephrodini/PyBer_Analysis/blob/main/Resources/total_fares_per_city_2.PNG).

Finally, an object-oriented line chart was created to better visualize the data in this dataframe. See [the resulting figure](https://github.com/josephrodini/PyBer_Analysis/blob/main/Resources/total_fares_per_city_chart.PNG). We can see a few things from this chart. First, ride fares seemed to spike across the board for a week in late February. Otherwise, no discernable trend can be seen that unites fare totals across the three city types; when some types are experiencing a higher fare total, others are low. Specifically, fares totals are lowest for urban and suburban areas immediately at the beginning of the year, while totals for rural areas are middling compared to other months.

## Summary

Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types. 

### Business Recommendations

Based on the analyses, it is recommended that PyBer:

- Try to attract more drivers in late February, when user ride fares are highest across the board.

- Expand marketing efforts for the beginning of the year in urban and suburban areas, when fare totals are lowest.

- Expand marketing efforts in rural areas to increase ridership.


### Limitations

The data analyzed was not for the entire calendar, more like quarter one of a year. It is recommended that more data be collected to see further trends as the year progresses. Also, more rider data could be collected such as average riders per trip and average tip per trip.