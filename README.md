# App Store Search & App Recommendations

## Overview
Recommendation engines are nothing but 'similarity hunters'. The search for similarity powered by NLPword2vec - is an astonishingly robust methodology. Depending on how one defines 'simialrity' between an item [or people, groups] we can develop a range of recommendation applications. The goal of this project is to recommend relevant apps in response to a search query. It uses semantic features to cluster similar apps (can be used for recommending apps or as a genre classifier). 

Some applications of this methodology could be,
* Purchase : When people buy X, they also buy Y
* Experience : When people buy read/watched/enjoyed X, they also enjoyed Y
* Location : When people who have been at/ate at/ stayed at X, they also went to Y
* Current Website : When people who came to this website, they also browse Y

## Goal
* Find relevant apps for a given query

## Methodology
For this project, we use a publicly available dataset on iOS App store apps. It has 7200 ios apps & their meta-data such as title, app description etc.  

* Step 1 : Tokenization & normalization of words in app description
* Step 2 : Represent words as embeddings using word2vec trained on Google News
* Step 3 : Calculate app vectors from app descirption
* Step 4 : Find nearest apps to a given query by using KNN 
* Step 5 : Visualize results using t-SNE

![You can view this presentation for more details](https://github.com/sroy4/App-Store-Search/blob/main/FinalPresentation.pdf)  
## Results
For visualization, I have used t-SNE (stochastic neighbor embedding) for visualizing high-dimensional data in a low dimension space. In this image below, you can see similar apps are assigned a higher probability for a given genre while dissimilar points are assigned a very low probability. Each cluster represents a genre of apps. 

![Clusters of Similar apps](https://github.com/sroy4/App-Store-Search/blob/main/Simialr%20App%20Clustering.png)


Let's take a look at results for the query "wedding party". All app results are related to a wedding party in different ways. The first result, Wedding Dash result is a wedding game. The second result, Big Day Lite is a countdown timer app for the wedding. The third result, LEDit is an LED banner app for the wedding. The fourth result, Open Table is an app for making restaurants reservations for the wedding. And the final result is Shutterfly, an app for creating wedding cards and photobooks. Word2Vec is able to account for deep semantic relationships between these apps.

![Results for the query "wedding party"](https://github.com/sroy4/App-Store-Search/blob/main/wedding_party.png)


![Results for the query "mystery games"](https://github.com/sroy4/App-Store-Search/blob/main/mystery%20game.png)
