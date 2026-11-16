## Update on Tasks/Progress Made:

The primary piece of progress made was that the datasets we chose for this project have been cleaned and optimized for research. The workflow for this process can be seen [using this link.](clean_datasets.ipynb)

The three CSVs were filtered together to only include flights at O'Hare International Airport in Chicago that departed in January 2026. Dates and airport codes were standardized. We also examined duplicates and missing values, ensuring such data issues were identified and corrected. Information about cancelled flights was kept, and delay values for them were left blank. The dataset for flights can be viewed [here.](flights_ord_jan2026_clean.csv).

The weather dataset was cleaned as well. Dates were standardized, and information about temperature, precipitation, wind speed, and visibility was kept for our use. That [dataset](
weather_ord_jan2026_clean.csv) was uploaded like the others to this repository.

Considering the limiting of the dataset to contain only scheduled flights at O'Hare Airport in January 2026, this shifts our existing research questions to where we will be more focused on illustrating the impact of weather on flight delays at this single airport pertaining to individual airlines. We had previously been more interested in researching weather and airport traffic relationships across airports. We will also have to look in detail at flights delayed or cancelled for reasons other than weather.

No work on visualization of data trends across the datasets has started.

## Updated Timeline:
Here is our updated project timeline, including the status of each task and when the task will be completed. Due to changes in our work plan and everyone's recent availability, due dates have been pushed back in comparison to the original planned timeline.

November 15 - At this point, everyone will pause on the project itself and begin working collaboratively on completing the Interim Status Report project. Parts will be assigned based off of everyone’s contributions to the project so far, with other work being distributed evenly and fairly. Complete Interim Status Report and submit before the assignment deadline. After, resume the project process. - All of the group members (Completed)\
November 19 - Join each of the three cleaned datasets together using common identifies and attributes. Ensure that no information is being lost in the process. Complete by this date. - Matthew (Not Started)\
November 22 - Midpoint meeting, confirm that data is ready for analysis and everyone is on the same page at this point in the process. Identify next steps for analysis and potential paths to take - All of the group members (Not Started)\
November 22 - Start analysis of the combined dataset, creating visualizations and statistics to help answer the research questions. - Alex (Not Started)\
November 29 - Complete analysis of the combined dataset, and finish answering the related research questions using the analyzed data. - Alex (Not Started)\
December 3 - Everyone will begin working on the final project submission and creating the final deliverable describing our accomplishments on this project. Parts will be assigned based off of everyone’s contributions to the project so far, with other work being distributed evenly and fairly. - All of the group Members (Not Started)\
December 06 - Final meeting, project should be all finalized at this point with all necessary points covered. We will meet to ensure that nothing else is missing and to make any final changes to the project. - All of the group members (Not Started)\
December 07 - Complete Final Project Submission before the assignment deadline. - All of the group members (Not Started)

Already completed: Clean each of the three datasets, making sure that there are no missing values, duplicate values, or errors. - Saanvi

## Changes to the Project Plan:
Regarding feedback from Milestone 2, we did not receive any specific requests to revise our original project plan. As a result, compared to our initial project plan, there have not been any major changes to our overall project objectives, research question, selected datasets, etc... However, to be transparent, our progress during this course projecet has been slower than initially anticipated, and we have not yet started or completed the data integration and analysis stages that we originally expected to have begun by this point. As a result, our original timeline will need to be adjusted to account for the remaining work and the limited time we have left before the final submission. The main adjustments we anticipate making involve revising our timeline and better organizing the remaining work to ensure that we can complete the project by the final submission deadline.

## Current Challenges or Problems:
One challenge was that the three datasets came in different formats. The OpenFlights file had no column headers, so I added them and used the airport code to find the O’Hare record. The NOAA file contained weather observations for 2026, so I filtered it to January to match the flight data. I kept the original observation times so the team can match them to scheduled departure times during the merge.

Another challenge was deciding what to do with missing departure delays. The cleaned flight dataset had 25,131 records, and all 909 blank departure-delay values came from canceled flights. I kept those flights and left their delay values blank so they could still be included when calculating the cancellation rate.

The next challenge is matching flights to weather observations because the scheduled departure times and weather timestamps may fall at different minutes. During the merge, we’ll check that the timestamps use the same time basis, then record how many flights match a weather observation and check that the merge doesn’t create extra flight rows. The cleaning steps and validation results are in the data cleaning notebook.

## Individual Contributions:
Matthew - Created the StatusReport.md file, and independently completed the "Updated Timeline" and "Changes to the Project Plan" sections to the Status Report.

Alex - Authored the "Update on Tasks/Progress Made."
