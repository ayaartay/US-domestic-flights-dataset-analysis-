# Analysis of US domestic Flights for 2008
## by Ainur Artay

## Dataset

The dataset "Data Expo 2009: Airline on time data" consists of more than 200 thousand domestic flights in the US. The attributes od the records include date of a flight, distance, arrival time and delay factors. The dataset (2008.csv), along with its explanatory documents, was downloaded from Harvard University's Dataverse website [here](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/HG7NV7).

## Summary of Findings

The following findings were observed:
* Arrival delay is caused by Departure Delay (before flight starts) and Elapsed Time Delay (in the airplane). Elaped Time Delay is the lag between Actual Elapsed Time and CRS(scheduled) Elapsed Time. This means how many minutes passengers had to spend their extra time in the airplanes.
* Departure Delay has far larger spread than Elapsed Time Delay.　
* Departure Delay is right-skewed, while Elapsed Time Delay is more symmetric. Both have means around zero.
* Neither Departure Delay, nor Elapsed Time Delay, have clear correlation with Distance.
* There are 5 delay factors which are in the dataset (NAS Delay, Late Aircraft Delay, Carrier Delay, Weather Delay and Security Delay. Security Delay was found to have very little effect on Arrival Delay compared to the other four factors, therefore, it was excluded from the analysis. 
* NSA Delay causes the majority of the delays, about 14%, followed by Late Aircraft Delay and Carrier Delay, 12% and 11%, respectively. 
* Neither of the four factors showed a clear correlation with Distance.
* Visualizations suggest that only NAS Delay is associated with longer Departure Delay.

```
* NAS Delay
Delay that is within the control of the National Airspace System (NAS) may include:  
non-extreme weather conditions, airport operations, heavy traffic volume, air traffic control, etc.   
Delays that occur after Actual Gate Out are usually attributed to the NAS and are also reported through OPSNET.

* Late Arrival Delay
Arrival delay at an airport due to the late arrival of the same aircraft at a previous airport.  
The ripple effect of an earlier delay at downstream airports is referred to as delay propagation.   

* Carrier Delay
Carrier delay is within the control of the air carrier. Examples of occurrences that may determine carrier delay are:  
aircraft cleaning, aircraft damage, awaiting the arrival of connecting passengers or crew, baggage, bird strike, cargo   
loading, catering, computer, outage-carrier equipment, crew legality (pilot or attendant rest), damage by hazardous goods,   
engineering inspection, fueling, handling disabled passengers, late crew, lavatory servicing, maintenance, oversales, potable   
water servicing, removal of unruly passenger, slow boarding or seating, stowing carry-on baggage, weight and balance delays.   

* Weather Delay    
Weather delay is caused by extreme or hazardous weather conditions that are forecasted or manifest themselves on point of   
departure, enroute, or on point of arrival.

* Security Delay  
Security delay is caused by evacuation of a terminal or concourse, re-boarding of aircraft because of security breach,      
inoperative screening equipment and/or long lines in excess of 29 minutes at screening areas.  

```

## Key Insights for Presentation

* The histogram of the distace shows that most of the domestic flights are relatively on short-distances. The observation that there's no clear correlation between delay factors and the distance could be affected by this facc, i.e. short-distance flights are overcrowding the long-distance ones. 
* There are way more delays than early arrivals (negative delays), which is shown by the right-skewed shape of the Arrival delay distribution. This makes sense as the planes do not depart early than the scheduled time and there's little room for the plane to significantly exceed the planned in air speed.
* The arrival delays can be caused: i) on land, prior to the start of the flight, i.e. delayed departure; and ii) in the air, i.e. longer elapsed time. 
* The comparison of these two delays in the scatterplot, the analysis of the attributes of the four delay factors in the barchart, and the violinplot of the delay times of the four factors was performed. This identified that the distance is not a significant factor to delay. 
* The main findings of this analysis were observed by using clustering Departure Delay and Elapsed Time Delay lengths in the violinplot.


