# PresidentialElection_Analysis
R 

### Background
The US presidential election in 2012 resulted in an unsurprising out come, meaning it went as predicted. However, the 2016 election took the nation by surprise. The results of the election showed that predicting voter behavior is complicated no matter the efforts put into collecting, analyzing, and understanding numerous available data sets.

### Purpose 
The purpose of this analysis was to merge the census data with voting data in 2016 to analyze the election's outcome. Using four datasets: tract-level 2010 census data, metadata, county-level vote tallies from the 2016 election, and raw election data, our goal was to clean the data sets and then perform further analysis and find the correct model that represents the outcome of the election optimally. 

### Process
We first cleaned the data sets exluding all NA values and then separated the raw election data into their repective states. We combined the votes for each candidate and created a new data frame with the organized structure. 
Using our now cleaned data we separated federal elections and state elections into two separate sets to break down the process in a simpler manor. From here we were able to find the state and county winners by taking the candidates with the highest proportions of votes and further separated them into "county_winner" and "state_winner" dataframes.
We were able to used the broken down frames to display on the map of the US whether each state and each county voted for the deomcratic or republican candidate.![states](https://user-images.githubusercontent.com/66536405/127402055-614cb20c-8ce0-43d0-bb72-cbf2014285cd.png)
![counties](https://user-images.githubusercontent.com/66536405/127402082-26252045-f795-4330-a765-0f8dfb96423a.png)
We then aggregated the census data to compare the result in the election to the demographic in a particular region. Using Santa Barbara as our location we saw a correlation with the demographic and the candidate who recieved the most votes.

In the PCA Machine Learning portion we scaled and centered the features and determined that in order to capture 90% of the variance in the data we needed to have 5 principal components This led us to finding that running heirarchial clustering for the first 5 components was the most appropriate. 

For the Classification Machine Learning portion we ran a few different models and found that our best results were with a log regression model based on the results of the ROC curve. This was due to the fact that Decision trees are very interpretable, but also very complex and can have large variation, which we do not want when we are trying to predict a candidate out of only 2 options.

However with further analysis using LDA and QDA methods we found no one model performs particularly well, with all models, including those of the decision tree and logistic regression, having a high false negative rate. This is an indicator that aligns with the widespread misprediction of the results of the election.
