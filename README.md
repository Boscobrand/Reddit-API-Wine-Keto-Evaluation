## PROJECT 3: PART A 

## EXECUTIVE SUMMARY - WEB API’S AND CLASSIFICATION



#### **PROBLEM STATEMENT:**


The Brand Marketing Team responsible for the Wine and Champagne Portfolio at international importer Pernod Ricard has been focused on aligning their brands with key trends in the marketplace, and on connecting with consumers as often as possible through different media environments.  


Most recently, one of their Brand Managers has become very active on Reddit and has had mixed success establishing conversations with consumers through posts in the subreddit r/wine.  After internal discussions, the Brand Team is interested in partnering several wine brands together with a focus on wine pairing with recipes for the Keto diet.  


The r/keto subreddit has a considerably higher number of users (1.7m compared to 106k in r/wine), and there has been some conversation about wine in their posts indicating a desire for this group to try new wine brands that fit their newly adopted lifestyle.  


The leader of the Brand Team is skeptical about translating their success to the r/keto subreddit and would like more information to help discern whether or not the posts on these two subreddits have more similarity than differences.  We have been called in to offer an analysis and perspective on both subreddits that could aid in an investment decision.


#### **OUR OBJECTIVES:**


- Use Web API’s and Classification Methods, collect a significant amount of posts from each subreddit to analyze
- Use Natural Language Processing and Text Feature Extraction methods, prepare the posts for classification
- Use Regression models to analyze and predict how similar or different the two subreddits may be based on Accuracy and using a Receiver Operating Characteristic Curve to assess.
- Share insights and recommendations with clients


#### **EXECUTIVE SUMMARY**


Capturing subreddit posts is a delicate balance of accessing a website’s API at the appropriate time, and appropriately filtering out text that can be evaluated through NLP and Text Feature extraction methods.  
After capturing over 7500 posts from the r/keto subreddit and over 2800 posts from the r/wine subreddit, the resulting dataframes were cleaned, balanced, and subjected to vectorization before two models were established.  

Features were held to the top 1000 most frequent terms, and assessed in a logistic regression model and a naïve Bayes model.  Ultimately, the Logistic Regression model was utilized for our presentation however the differences between the performance of the Logistic Regression model and the Naive Bayes model was negligible.

We observed a very distinctive difference between both subreddits in our model.  First, the distribution of predicted outcomes clearly exposed the Keto and Wine datasets to be aligned at separate ends of our histogram, with all features of r/wine predicted to be True Positive and all features of r/keto predicted as True Negative, with little to no overlap.  Our accuracy score predicted 98.9% of our observations correctly .  Our Sensitivity score indicated we were correctly predicting positives at 99.2%.



|                         |    LOG     |     NB      |
|------------------|-------------|------------|
|  ACCURACY   |   98.4%   |   98.9%  |
|  SENSITIVITY  |  99.2%   |   99.3%   |
|  SPECIFICITY   |  98.0%   |   98.4%   |
|  ROC AUC       |  99.8%    |  99.8%    |


#### **FINAL CONCLUSIONS AND RECOMMENDATIONS**


At this time, promotionally activating r/keto for any brand does not appear to be viable without further analysis.  The concept could prove to be a great marketing opportunity to “wine pairing” awareness among devout followers of Keto, however the r/keto subreddit may not be the most advantageous forum to engage those consumers in.


We would recommend that it could be worthwhile to consider evaluating other subreddits that may exhibit more similarity to r/wine, such as r/weight watchers (41k users), r/loseit (2.0m users), or r/nutrition(684k users).  In addition, consideration could also be extended to other social media platforms that offer higher levels of text based engagement through similar channels.



#### **CONTENTS**


-	NOTEBOOK A: EXECUTIVE SUMMARY (THIS NOTEBOOK)
-	NOTEBOOK B: COLLECTION OF KETO AND WINE POSTS THROUGH PUSHSHIFT IO
-   NOTEBOOK C: CLEANING OF KETO AND WINE PUSHSHIFT IO CAPTURES
-	NOTEBOOK D: COMBINED KETO & WINE FILES, EDA, AND MODELING


#### **SOURCE DOCUMENTATION**


-	[keto_push_clean.csv](*keto_push_clean.csv*)
-	[wine_push_clean.csv](*wine_push_clean.csv*)
-	[keto_push_output.csv](*keto_push_output.csv*)
-	[wine_push_output.csv](*keto_push_output.csv*)


*“A ketogenic diet for beginners” by Dr. Andreas Eenfeldt, MD*

https://www.dietdoctor.com/low-carb/keto


*“Keto alcohol – the best and the worst drinks” by Dr. Andreas Eenfeldt, MD*

https://www.dietdoctor.com/low-carb/keto/alcohol-guide

