## Overview:
Our project will explore how weather conditions and airport traffic relate to flight delays and cancellations at selected U.S. airports. We want to identify patterns in flight disruptions and compare how reliably airports operate during similar poor weather conditions.

We plan to combine NOAA Local Climatological Data, BTS Airline On-Time Statistics, and a third dataset containing airport traffic volume. These datasets will provide information about local weather, flight performance, and how busy each airport is. We will select airports and a time period with overlapping data coverage.

Before combining the datasets, we will check for missing values, duplicate records, inconsistent formats, and differences in measurement units. We will match weather stations to airports and connect weather observations to flights using their scheduled departure dates and times. Airport traffic data will be linked using airport identifiers and matching months. After that integration we will check for unmatched records and unexpected changes in record counts. Finally we will create summary statistics and visualizations to compare delays, cancellations, and on time departure rates across airports.
## Team: 

Tasks and roles are distributed accordingly with each member’s individual strengths, interests, and availability in mind. These roles may be adjusted if a member encounters any difficulties or conflicts when approaching their assigned work. Everyone will participate in the documentation process and work collaboratively with each other to ensure cohesiveness.

Saanvi: Will be in charge of finding and collecting 3 related data sources for our project. They will also document where the data came from and the process that they took to collect each piece of data.

Inseo: Will handle cleaning the data and ensuring that there will be no major difficulties or errors when eventually utilizing the data. Includes resolving missing values, duplicate entries, standardizing formats, etc… Will also document the changes that they made to the data and the decision making process.

Matthew: WIll handle identifying common attributes among each of the data sets and combining all the dataset into one cohesive one for analysis. Will ensure that no important information is missing, misinterpreted, or lost. Will also document the combination process and any decisions made during it.

Alex: WIll handle analysis of the combined dataset and utilizing the data to answer our project’s research questions. Includes creating any important visuals, statistics, or graphs that will impact or is important to the analysis process. Will also document their results and their thought process behind their analysis.

## Research or Business Questions: 
How do weather and airport traffic relate to flight delays, and which airports are most reliable during poor weather?

## Datasets:

## Timeline: 
Here is a draft of our project timeline, including what is required, when the task should be complete, and who will be completing it.

October 18 - Clean each of the three datasets, making sure that there are no missing values, duplicate values, or errors. - Inseo\
October 25 - Join each of the three cleaned datasets together using common identifies and attributes. Ensure that no information is being lost in the process. - Matthew\
November 1 - Midpoint meeting, confirm that data is ready for analysis and everyone is on the same page at this point in the process. Identify next steps for analysis and potential paths to take - All of the group members\
November 8 - Start analysis of the combined dataset, creating visualizations and statistics to help answer the research questions. - Alex\
November 15 - At this point, everyone will pause on the project itself and begin working collaboratively on completing the Interim Status Report project. Parts will be assigned based off of everyone’s contributions to the project so far, with other work being distributed evenly and fairly. - All of the group members\
November 19 - Complete Interim Status Report and submit before the assignment deadline. After, resume the project process and work towards finishing analysis. - All of the group members\
November 22 - Complete analysis of the combined dataset, and finish answering the related research questions using the analyzed data. - Alex\
November 29 - Everyone will begin working on the final project submission and creating the final deliverable describing our accomplishments on this project. Parts will be assigned based off of everyone’s contributions to the project so far, with other work being distributed evenly and fairly. - All of the group Members\
December 06 - Final meeting, project should be all finalized at this point with all necessary points covered. We will meet to ensure that nothing else is missing and to make any final changes to the project. - All of the group members\
December 07 - Complete Final Project Submission before the assignment deadline. - All of the group members

## Constraints:

The biggest constraints include the lack of information on individual flights in the OpenFlights data, as this dataset specializes in providing identification information on routes. This still provides valuable indexing information that is more comprehensive than the on-time statistics. These two datasets are therefore good complements. The Bureau of Transportation Statistics website splits data on Departures, Arrivals, Airborne Time, Cancellations, and Diversions, into separate tables, and they are all voluminous datasets that may be unwieldy to download and work with. That will cause problems. These may include “downloadability” problems pertaining to certain spatiotemporal limitations (for example, it may only be possible to download data over time intervals of one month). 
Furthermore, merging flight information datasets with local climatological data will be a difficult process, as it will require data calculated on hourly intervals in order to accurately measure the impact of weather on individual flights (as we know, weather can change quickly in a given day). Again, this amount of data is simply enormous, and over a large area, this may be technically difficult to manage and integrate.

## Gaps:

We will certainly learn a lot on our own and as a group while working on the data integration and how to conceptualize that conversion. We also may have to compromise on whatever timeframe we determine for the project due to the sheer amount of flights in American airspace daily, which would all ideally be tied to climatological data as a supplement to data on flight delays, cancellations, and the amount of time flights took. 
