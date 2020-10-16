# A2 Bias in Data
By: Matthew Rhodes
Date: 10/16/2020

## GOAL
### For this assignment, the goal is to identify potential sources of bias in a corpus of human-annotated data, and describe some implications of those biases. 

This project is centered around Wikipedia's [Detox](https://meta.wikimedia.org/wiki/Research:Detox) research. "In collaboration with Jigsaw, Wikimedia Research is developing tools for automated detection of toxic comments using machine learning models. These models allow us to analyze the dynamics and impact of comment-level harassment in talk page discussions at scale. They may also be used to build tools to visualize and possibly intervene in the problem." An example of one of these tools is [Perspective API](https://github.com/conversationai/perspectiveapi).


## Data
***
The corpus used is called the Wikipedia Talk corpus, and it consists of three datasets. Each dataset contains thousands of online discussion posts made by Wikipedia editors who were discussing how to write and edit Wikipedia articles. Crowdworkers labelled these posts for three kinds of hostile speech: “toxicity”, “aggression”, and “personal attacks”. Many posts in each dataset were labelled by multiple crowdworkers for each type of hostile speech, to improve accuracy. For this repo I used the “toxicity” and “aggression” datasets. <br>
The toxicity and aggression datasets can be downloaded from figshare [here](https://figshare.com/projects/Wikipedia_Talk/16731)

## Questions to detect bias
To detect bias in this dataset I wanted to answer the following questions:

1. (A) Demographics have a different idea of what agression is (not uniform distribution)
   (B) The same question but for toxicity
   
2. (A) Annotators from high school will label less comments as agressive than annotators with a master's or doctorate.
   (B) The same question but for toxicity
 
   
3. There will be a positive linear correlation between the number of aggressive labeled comments and toxic labeled comments when grouped by age.

4. There is an even distribution of answers from the age and education demographics.

## LICENSE
***
To align with the access policy of the data found here: https://foundation.wikimedia.org/wiki/Open_access_policy <br>
Any aggregated and properly anonymized data produced as part of the project is under CC0; <br>
All source code is under the MIT License; <br>
Any media files are under Creative Commons Attribution-ShareAlike 3.0. <br>

## Analysis
***

#### As you can see from the three bar charts below the answer to question 1 is that the different demographics have varying ideas of what toxic/aggressive comments are, there is not a uniform distribution across the different ages, education levels, or genders.

#### From the top right graph we can see that I was wrong with my assumption for question 2. High school students labeled more comments as toxic/aggressive than people that had a masters degree or doctorate. Regarding question 3 there is a positive linear correlation but it is not strictly positive. Generally as someone gets older, the amount of comments they perceive as aggressive is linearly correlated with the amount of comments they perceive as toxic.

![alt text](https://github.com/MatthewCodes/data-512/blob/main/data-512-a2/first_graph.png)


#### To answer question 4, we can see from the charts below we can see that there is a clear bias in the people selected to participate in this annotation process. There is a significant amount of more people that only completed highschool or got their bachelors degree than any other category. In line with this there is a significant amount of more people that are from ages 18-30, or 30-45 than any other age group. The result of this bias is that these comments are mainly viewed as toxic or aggressive by young people. This means that any model created on this dataset will only find comments that younger people think are negative completely ingoring comments that older generations and highly educated people think are negative.

![alt text](https://github.com/MatthewCodes/data-512/blob/main/data-512-a2/second_graph.png)
