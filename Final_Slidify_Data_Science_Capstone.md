---
title: "Final Slidify Data Science Capstone"
author: "Chongyuan Xu"
highlighter: highlight.js
output: pdf_document
job: Postdoctor
knit: slidify::knit2slides
mode: selfcontained
hitheme: tomorrow
subtitle: A Method to Predict Stars by a Review of a Business
framework: io2012
widgets: []
---

## The Questions to Answer

The following table demonstrates the number of each stars rated by customers from the historical review data. 


```
## 
##      1      2      3      4      5 
## 159811 140608 222719 466599 579527
```

So it is intersting to find what is the relationship between the review and its rate? What are the most frequent positive and negative words in the reviews? 

--- .class #id 

## The Most Frequent Positive and Negative Words

I use NLP algorithms to find the common words and they can be seen in the following barplots. 

![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png) 

--- .class #id

## The Grade Predicted by any Review Text

I create the word frequency matrix first and then design an algorithm based on SVM to predict the grade by text data according to machine learning techniques. 


```
## Confusion Matrix and Statistics
## 
##           Reference
## Prediction good medium poor
##     good   2444    210  105
##     medium  336    192   89
##     poor    554    278  793
## 
## Overall Statistics
##                                           
##                Accuracy : 0.6857          
##                  95% CI : (0.6726, 0.6985)
##     No Information Rate : 0.6667          
##     P-Value [Acc > NIR] : 0.002207        
##                                           
##                   Kappa : 0.4298          
##  Mcnemar's Test P-Value : < 2.2e-16       
## 
## Statistics by Class:
## 
##                      Class: good Class: medium Class: poor
## Sensitivity               0.7331       0.28235      0.8034
## Specificity               0.8110       0.90164      0.7927
## Pos Pred Value            0.8858       0.31118      0.4880
## Neg Pred Value            0.6030       0.88869      0.9425
## Prevalence                0.6667       0.13597      0.1974
## Detection Rate            0.4887       0.03839      0.1586
## Detection Prevalence      0.5517       0.12338      0.3249
## Balanced Accuracy         0.7720       0.59200      0.7981
```

--- .class #id

## Results and Future Works

It is seen that the accuracy is just 70 percent, although it is the highest algorithm among my experimental results. To be honest, this is not a bad result. However, we still need to research some new tools to improve the accuracy. 



