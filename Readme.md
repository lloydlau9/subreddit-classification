# Project 3: Web APIs & NLP 

## Contents:
- [Executive Summary](#Executive-Summary)
- [Problem Statement](#Problem-Statement)
- [Data Dictionary](#Data-Dictionary)
- [Conclusions](#Conclusions)
- [Recommendations](#Recommendations)

## Executive Summary

Based on the home page of Reddit, it describes itself as a place for community, conversation and connection with millions of users worldwide in addition to Reddit being a community of millions of users engaging in the creation of content and the sharing of conversation across tens of thousands of topics.

Reddit is where very often, there are always topics or ideas discussed and shared, and more importantly these are arranged in communities. It permits the joining of everyone’s favourite communities which will create a constant, personalized feed of content like news headlines, opinions, stories, both fun stories and startling discoveries, sports talk, games, viral pics, top memes, and videos.

There are several reasons why Reddit is such a sought after search medium. Primarily, people from all walks of life access Reddit is to seek, understand and participate, whether actively or passively, on an infinite number of themes, concepts and circumstances. These include those that appear to be controversial, undisputable, indefensible or just simply those with no answers at all.

With the above in mind, Reddit is considering to venture into the categorisations with the inclusion of issues.

One of the issues would be relating to diets which are further sub-categorised into features with vegan diets as opposed to ketogenic diets in co-relation to life-style aspects and the serious health aspects
## Problem Statement

The goal of this project is to address the popularity of diet advices through classification from two subreddits, “Vegan” and “Keto”.

The focus is to scrape two subreddits and create different types of classification models such as Naive Bayes Classifier and Logistic Regression Classifier then to compare between models. Through this modelling process, this will then determine the mostly used observed textual data to be classified under which group of subreddit.
From the results to then measure the classification metrics on accuracy, misclassification rate, sensitivity and specificity obtained from the model scores.

The success will be evaluated by the model scores based from the test scores and the least difference between both training scores and test scores of the accuracy.

These will be addressed to the Plant Based Producers and Health Professionals as the main stakeholders as they are the ones who care about the environmental sustainability - do we eat less beef cos we care about the environment or eating healthy but need to think of the  health of the planet Earth.

As for the secondary stakeholders are environmentalists (those who care about protecting environment, climate and the planet)  animal rights activists (ie those who care about protection of animals)

## Data Dictionary

| No | Features/ ID             | Type        | Description                                          |
|----|--------------------------|-------------|------------------------------------------------------|
| 0  |   subreddit              | object      |  Subreddit category                                  |
| 1  |   id                     | object      |  ID number                                           |
| 2  |   author                 | object      |  Author created the post                             |
| 3  |   title                  | object      |  Title text of post                                  |
| 4  |   selftext               | object      |  Text details of post                                |
| 5  |   subreddit_subscribers  | int         |  Subreddit Subscribers                               |
| 6  |   created_utc            | int         |  Created Coordinated Universal Time                  |
| 7  |   created_time           | object      |  Time that was Created                               |
| 8  |   length_of_time(sec)    | int         |  Seconds                                             |
| 9  |   num_of_comments        | int         |  Number of comments                                  |
| 10 |   score                  | int         |  Score                                               |
| 11 |   text                   | object      |  Merged text of "title" and "selftext"               |
| 12 |   post_length            | int         |  Length of post                                      |
| 13 |   text_cleaned           | object      |  Cleaned up text data                                |


## Conclusions

It was observed from the evaluation metrics that **the *MultinomialNB* model with *CountVectorizer* has a very high classification accuracy on the testing score**. 

Looking at the *Sensitivity* and *Specificity*, and the numbers of false positives and false negatives, it can be seen that the subreddits vegan and keto are classified properly that only a few posts are mis-classifed. In general, both subreddits have similar posting rate per day and simlar length of per post, but **the subscribers and comments for keto are higher than vegan**, this indicates that more people are interested in keto than vegan as a trend.

Also, those who are into vegan diets are confident and have stable views about this whilst there is more curiosity and arguments about keto diets.


### Recommendations

It would be recommended to review on the misclassified posts keywords prior to postings in vegan forum and to possibly increase the breath of the timeline of the data collected to capture more insights of different subreddits.