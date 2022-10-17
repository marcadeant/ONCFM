# ONCFM
Machine learning supervized algorithm to detect fake money. ONCFM is french for Organisation Nationale Contre la Fausse Monnaie.

# Introduction

It could be fastidious for a human being to detect by it-self if it's either a fraud or a conform banknote. Even if credit card payment system is the most used and sophisticated way to pay, especially with e-commerce's rises, still merchants (bookstore, grocery, supermarket...) use traditional old-fashion means of payment : cash.   For this reason, I designed and built an **artifical intelligence** ables to identify the true nature of a traded banknote.

# Learning on characteristic data 

In this section, I will explain what the data looks like before feeding and training the machine learning models. Before starting with the data presentation, there are 2-differents ways of thinking. 

1. Use of **image detection** machine learning algorithm to split on fake/true banknote samples.
2. Use of **banknote dimensional parameters** to determine the perfect fake/true banknote profil. 

For the purpose of this project, I worked with the banknote dimensional parameters. Indeed, data sample that I used shaped like banknote as rows and 6-dimensional parameters as columns and an `is_genuine` extra-columns. Feel free to check-out the whole [data csv](https://github.com/marcadeant/ONCFM/blob/main/Data/billets.csv)

Every american banknote was described as follow :

1. `height_left` : banknote left vertical side in mm 
2. `height_right` : banknote right vertical side in mm 
3. `margin_low` : distance between US president picture and lower edge 
4. `margin_up` : distance between US president picture and upper edge
5. `lenght` : banknote horizontal side in mm
6. `diagonal` : banknote diagonal size in mm

