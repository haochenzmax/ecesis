# Q2 Summary Report
## Define Functions
For the purpose of not hard-coding, all of the implementations are by functions in this task. We just have to type in specific column names of different files for it to be re-usable.
## Preprocessing One-appliance Sheet
1. Convert watt to kilowatt
2. Convert time column to standard datetime column
3. Sum the rows on an hourly basis
## Preprocessing Large Sheet
1. Define function called "twentyfour_to_zero" which converts "24:00:00" to "00:00:00" of the next day.
2. Apply the aboved function to large sheet's time column.
3. Convert time column to standatd datetime column by adding the year appeared in one-appliance sheet, since we'll have to merge them based on time index.
## Merge datasets
1. Merge the two preprocessed datasets by their index using a outer join.
2. Create a column containing sum of all electricity consumption for each hour interval.
3. Plot the data by hour/weekday/month.
## Conclusion and Observation
From the plots we can observe that:
1. From a day's span, we observe that the peak hours occurr from 10am - 3pm. This could be the most active hours of a day, and it could also be the most demanding hours of air conditioning.
2. From a week's span, the lowest consumption occurs on Wednesdays, then increasing to the peak on Sundays and falling back till Wednesdays. I guess that's because electricity is consumed more as it approaches to weekends.
3. From a year's span, high consumptions occurr in winters and summers, while significantly lower in springs and falls. I will have to give it to the high demand of air conditioning in the former two seasons.
