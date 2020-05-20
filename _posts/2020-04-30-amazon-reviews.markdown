---
title:  "Amazon Reviews Project"
subtitle: "Text Analysis"
author: "Sally Akuffo"
avatar: "img/author/mesmaller.jpg"
image: "img/woodtype.jpg"
date:   2020-04-30 2:12:12
---
### Problem Definition
Amazon.com is the world’s largest online marketplace. It focuses on e-commerce, cloud computing, digital streaming, and artificial intelligence. For this case analysis, a large dataset was provided with reviews from Amazon’s products by its customers. The goal of this analysis is to gain insights from customer reviews by employing sound Machine Learning techniques. To find out if the reviews written match up with the numerical ratings given. 

## Text/ Data collected
The Amazon reviews data set is a comma separated file(csv) that has 3 columns and 3,000,000 rows. Of the 3 columns, the first column consisted of numerical Ratings from 1 to 5, the second column consisted of short titles of the products that were purchased, and the third column had the written reviews of the consumers of the products. Due to slow processing time a sample of 250,000 rows was initially used  but this had to be further reduced to 30,000 rows of data.

### Analysis Process
Text Organization
The Amazon reviews csv file was imported into python as a data frame. The column containing the reviews description was filtered out as a separate data frame then converted into a list.
To clean up the text a list of stop words were generated to remove frequent words and unnecessary words. Then the text was tokenized to prepare  the text to be converted into a DTM

### Tokenizing
The text to be converted into a DTM using the frequency analysis and the weights analysis.
then it was converted into a DTM using the countvectorizer in Python.

### DTM
To analyze the text, various machine learning algorithms were applied to the text. I chose to use the frequency DTM  for the rest of the process .The DTM was, first, standardized due to its sparseness to normalize the data. After wards Dimension reduction techniques were applied to the data.

### Dimension reduction
The Dimension reduction techniques used were PCA, Sparse PCA, t-SNE and UMAP.
Out of the three I chose to use t SNE because the data set was already large and t-SNE gave the fewest components.
Classification Modeling
Next, the t -SNE output was divided into train and test set and was used to run Classification models. The classification models used were KNN, Random Forests, XG Boost, and gradient boosting. The accuracy scores for these models were low ranging between 22% and 26%. Out of all the algorithms XG boost and gradient boosting gave the highest accuracy scores. 
Sentiment Analysis
Polarity and sentiment analysis were then performed to compare to the results of the supervised learning algorithms and clusters were created from those.

[![foo](https://live.staticflickr.com/65535/49875679882_2f380afe4f_n.jpg)](https://flic.kr/p/2iZkTZd)

[![foo](https://live.staticflickr.com/65535/49916259561_46e7ccb159_w.jpg)](https://flic.kr/p/2j3VSUR)

## Visualization of Clusters
[![foo](https://live.staticflickr.com/65535/49875325331_e14c6cf2f1_z.jpg)](https://flic.kr/p/2iZj5Ag)

## Insight 
The visualizations from the classification models compared to the clustering based on sentiment Analysis shows that the sentiment analysis performed better and would be best to train a predictive model based on these clusters. 
Overall, the clusters were a mixture of all ratings it was not detected that one rating belonged to a specific cluster as a result. We can say that a negative or positive review does not necessarily lead to a certain numerical rating. 

