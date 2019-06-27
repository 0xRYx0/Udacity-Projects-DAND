# USA Flights Data Exploration

## Dataset

This dataset reports flights in the United States, including carriers, arrival and departure delays, and reasons for delays, from 1987 to 2008. The data comes originally from [RITA](https://www.transtats.bts.gov/OT_Delay/OT_DelayCause1.asp) where it is [described in detail](https://www.transtats.bts.gov/Fields.asp?Table_ID=236). These files have derivable variables removed, are packaged in yearly chunks and have been more heavily compressed than the originals.

In total, 23 csv files have been downloaded, decompressed and marged during this study. The process of combining those files took around (6.4) mins to generate a **giant DataFrame** called __[df_flights]__ that has **[123,534,969]** entries (rows) each with **[29]** variables (columns). This dataframe will be used during the wrangling and analyzing process.

## Summary of Findings

Over the years the number of flights has been increased and it's predicted to keep increasing. Seems like the overload of the flight is generally equally distributed among the months. I was expecting to see a huge difference between summer and other months. The current difference is about **800K** flights. In the last day of the month **day 31** has the lowest number of flights, this is due to the fact that only **7 months out of 12** have 31 days. Interestingly, **Saturday** has also the lowest number of flights with almost **3 million** flights.

Overview of US airlines showed that **[29]** carriers have been busy operating **[123,534,969]** over the last **23 years**. As shown above, there was a jump on **1988** and this is expected due to the increase in the number of carriers and the boom in economic activity in aviation.

What really caught my eyes is what happened in **2002**?! There is a slight drop in the number of flights with almost **[700K]** flights and some carriers, such as **("AQ","Aloha Airlines Inc.")** were disappeared!! Searching the company [Wiki's page](https://en.wikipedia.org/wiki/Aloha_Airlines) attributed this to what happened in [September 2001](https://en.wikipedia.org/wiki/September_11_attacks).

The strongest correlation is between Departure/Arrival Delays from a side and the delay source from the other side. Unexplained white areas were shown also at the middle of the graph.

An approximately linear relationship was observed when plotting scattered plot to illustrate the correlation between Departure delay and Arrival delay, which make sense as the flight will arrive late once there are some issue while take-off. Also, It has been noticed that the main cause of delay in the world of aviation is usually the carriers, that followed by the weather as second main cause of flights cancellation. Moreover, as most of the flights have been managed to be operated on the scheduled time, many graphs showed a stable performance and anomalies where easy to be detected.
