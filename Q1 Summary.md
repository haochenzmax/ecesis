# Q1 Summary Report
## Daylight Saving Time
First we define a function which identify whether the current date and iso type fall into daylight saving time (excluding MISO).
## NERC Holidays
Then we define a function which takes in a year and calculate the dates for all 6 nerc holidays of that year.
Notice that New Year, Indepedence Day, and Christmas are fixed dates, while Memorial day, Labor Day, and Thanksgiving are not fixed so that we'll have to calculate them for every year.
## Period Parsing
After that we define a function which parses the period character in out later "get_hours" function. Since we only have certain format (e.g., 2019-01-01, 2019Mar, 2019Q1, 2019A), we identify each case and get the start and end dates for that period.
## get_hours
Then we started to implement the get_hours function. First we define peak types for all 7 regions. There are minor differences among those, such as some peak hours are weekdays 7am - 10pm, some are 8am - 11pm, and California is Mon - Sat 7am - 10 pm.
We iterate through each date to identify which peak type it is, and we have to account for some special circumstances. For instance, for "onpeak", weekends and holidays are skipped; for "offpeak", weekends and holidays should be 24hrs counted, etc.
Last but not least, if that date is when we switch between daylight saving to normal time, we minus or add one hour.
## Conclusion
This is a very interesting task. I spent most of the time trying to search for definitions of peak types for various isos and thinking of logics behind daylight saving time, calculation of holidays, and how we play with hours inside the get_hours function.
