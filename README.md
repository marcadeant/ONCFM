# ONCFM
Machine learning supervized algorithm to detect fake money. ONCFM is french for Organisation Nationale Contre la Fausse Monnaie.

# Introduction

It can be difficult for a human to detect if it's either a fraud or a conform banknote. Even if credit cards is the most used and sophisticated way to pay, especially with e-commerce's rises, still merchants (bookstore, grocery, supermarket...) use traditional old-fashion means of payment : cash.   For this reason, I designed and built an **artifical intelligence** ables to identify the true nature of a traded banknote.

# Learning on dimensional features

In this section, I will explain what the data looks like before feeding and training the machine learning models. Before starting with the data presentation, there are two different ways of thinking. 

1. Use of **image detection** machine learning algorithm to split on fake/true banknote samples.
2. Use of **banknote dimensional parameters** to determine the perfect fake/true banknote profil. 

For the purpose of this project, I worked with the banknote dimensional parameters. Indeed, all data point that I used were shaped like banknotes. It means 6-dimensional parameters for columns with an `is_genuine` extra-column. Feel free to check-out the whole data csv [here](https://github.com/marcadeant/ONCFM/blob/main/Data/billets.csv).

Every american banknote is described as follow :

1. `height_left` : banknote left vertical side in mm 
2. `height_right` : banknote right vertical side in mm 
3. `margin_low` : distance between US president picture and lower edge 
4. `margin_up` : distance between US president picture and upper edge
5. `lenght` : banknote horizontal size in mm
6. `diagonal` : banknote diagonal size in mm

# Machine learning models build and results

Remaning, I used dimensional data featured that allows us to build a regression model instead of a image-based model.
Please take a look at the top of my [classification models notebook](https://github.com/marcadeant/ONCFM/blob/main/Notebooks/Classification%20models.ipynb) to get well-informed on **logistic regression** method. 
You can go straight to the result and see how well our regression logistic is performed.

In addition, I tested **clustering** approach in order to improve my model forecast accuracy and compare it with the previous methods. Even if both of these methods have good results, logistic regression is the most suitable model for my data.

# Results and true/false banknote profiling

![banknote_profiling](https://github.com/marcadeant/ONCFM/blob/main/banknote_profiling.PNG)

**Comment** : Profiling between true and false banknote's nature show us that `margin_low` and `lenght` are both good features for our models predicting the correct answer. 

Accuracy speaking, I let you take a look at logistic regression and clustering models performance with **confusion matrix** I made to compare these 2-differents artifical intelligence approach. 

![performance array](https://github.com/marcadeant/ONCFM/blob/main/performance_array.PNG)
