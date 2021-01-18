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

## Methodlogy
For this project, we use publicly available dataset from Mobile App statistics. It has 7200 ios apps & their meta-data such as title, app description etc.  

* Step 1 : Tokenization & normalization of words in app description
* Step 2 : Represent words as embedings
* Step 3 : Calculate app vectors 
* Step 4 : Find nearest apps to a given query by using KNN 
* Step 5 : Visualize results using t-SNE
