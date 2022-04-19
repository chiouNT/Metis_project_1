# EDA project: The subway ridership changes: an insight for the street vendor’s reopening

## Abstract

A lot of the street vendors located nearby MTA stations have shut down their business since the pandemic in March, 2020. In addition, COVID-19 outbreak has led to the changes of the subway ridership in New York city.  Thus, the information of the ridership changes can provide reopening strategies for the street vendors. To achieve this goal, the changes of the ridership before and after the outbreak were calculated. The analysis showed that most of the stations with the high ridership reduction are located Manhattan borough. In addition, the ridership dropped more in the weekday than in weekend.

## Design

    Most customers for the street vendors nearby MTA stations come from the commuters. Thus, it makes sense to use the ridership of stations as an indicator of the amounts of the customers. It also makes sense to use the counts of entries of turnstile to represent the ridership. 
    COVID-19 outbreak occurs on March 2020. Thus, two time points, March 2019 and March 2022, are chosen to be the representative before and after the outbreak, respectively. The ratio of the monthly ridership of these 2 time points represents the ridership changes. This strategy allows to identify the stations with the high and low ridership reduction. The daily ridership across a week of these stations is then profiled to determine the daily ridership changes due to the pandemic. 


## Data
* The MTA turnstile dataset 
  * [Link: Turnstile Data](http://web.mta.info/developers/turnstile.html)

* Geographic data of MTA stations
  * Correlation of station name to complex id [Link: Detailed Annual Sales Reports by Borough](http://web.mta.info/developers/data/nyct/subway/Stations.csv)
  * Correlation of complex id to borough [Link: https://qri.cloud/nyc-transit-data/remote_complex_lookup)
  
## Algorithms

* Filter MTA dataset to contain the data of 3/1-3/31 of 2019, 2020 and 2022.
* Covert the cumulative values of the entries to daily values.
* Use the functions to remove the errors of the counts of the turnstiles.
* Aggregation the data at the station level to get the monthly entry values.
* Calculation of the ratio of the monthly entry values.


## Tools
* SQLAlchemy: load SQL tables are load into Python
* Pandas: Data cleaning and analysis
* Matplotlib: data visualization
* Numby: generation of the positions of bar on X axis


## Communication
* •	Most of the stations with the high ridership reduction are located Manhattan borough and one of the stations shows that the ridership dropped more in the weekday than in weekend. Thus, these street vendors may consider to relocate or reduce their business scales.


![image](https://user-images.githubusercontent.com/71529189/116646421-00228800-a946-11eb-828f-de34c8045a81.png)

![image](https://user-images.githubusercontent.com/71529189/116648147-585b8900-a94a-11eb-9afd-6a698e32b31d.png)