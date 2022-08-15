# Capstone-Project


Introduction

For my capstone project, I will be creating a predictive model using drug overdose death data. Using this model, the healthcare industry would be able to more accurately distribute Naloxone (the drug used to reverse overdoses), and educators would be able to introduce a program to better educate children in high-risk areas. In this paper, two sources will be evaluated. These sources describe two machine learning projects that were done to predict opioid overdoses. 

Literature Review

The first project used random forest classification to predict OUD (Opioid Use Disorder) in adults. This was done using a 2016 NSDUH survey. The survey included questions about first time opioid use and the dataset used included 11 features (Mukherjee, 2020). These eleven features include: gender, age, race, income, employment, education, disability, mental illness, first use of alcohol, first use of marijuana, and overall health (Mukherjee, 2020). The creator of this project used these answers to the survey in order to predict how likely one was to develop OUD in adult life (Mukherjee, 2020). The creator mentions that prior marijuana use was a large indicator in predicting whether or not someone would develop OUD in their adult life (Mukherjee, 2020).
The second project used machine learning and internet search trends to predict short term overdose deaths. This project used public drug overdose data published by the State of Connecticut in order to build a predictive model (Wadekar, 2019). The goal of this project was to predict weekly drug overdoses in the state of Connecticut (Wadekar, 2019). 

Datasets

https://dataplanet-sagepub-com.mutex.gmu.edu/dataset?view=AAsBXQAAgAB%24AQAAAAAAAAAA3_zMslwIJ8Ve1X%24GFkbpBG2ii7wZFl1SDLeAXlWdsBrV8L5mgAm_Aa1tMRoxYItMyIl7f7BkADLg%244waNNIOcm9xoW3z4pDu9FcJQPlLjV6MuvXufqb8g42mq4uMdK8qL2OL7cqq3h6ZlaAn20eK4gyvjXXf7BRDqmF_ksLdfE5vfqd3WFWwlheA4JIBFSP25LRBfmp0vaIwpQrP6gAzLktw4pTUmaNHfH3H0PHgBdE7L0jKcAA

https://dataplanet-sagepub-com.mutex.gmu.edu/dataset?view=AAsBXQAAgABzAQAAAAAAAAAA3_zMslwIJ8Ve1X%24GFkbpBG26TF3NmlXs3tXjCLf731SFGMXvHv2gMwDR2RgGngIBxbYHBDTtv196xNTojaKBAtNt%24Tx6XgwMGFPhBrwt5%24UaJ9A_e2NhoZRm2Fi0jcbD4xIjW4svpwHEfYWTMZels%241IeVlAgzg%24L38Oa4uSUQHDSSqnzhr3HUZpRxk5kZ5IRYwJGMdbSDeJyS9s2n6J05IECjUOP2NJM5IYQlE

Github Repository

https://github.com/tmbibler2/Capstone-Project


Exploration of Data




2020
2019
2018
2017
2016
mean


977.65
917.28
933.27
828.37
median
2948
558
444
456
466
Standard deviation
1399.67
1005.37
933.43
971.68
846.70
IQR
1655.5
1152
1050
1030
976
min
101
39
28
35
42
max
978
3771
3237
4293
3613



Above is the summary statistics for the drug overdoses by state dataset. My main variables of interest is the number of deaths and state variables. Crude rate and age adjusted rate will most likely be discarded unless I see a need to use it later on in the project. The code I used to clean and calculate these statistics have been pushed to my Github repository. 

Methods

For the cleaning and calculations of the data, I used RStudio and uploaded it to an Rmarkdown PDF. For the actual predictive model, I will be using Python. 

In order to create my model, I will most likely be using supervised machine learning because my data points have labels. The model will predict the amount of overdose deaths by state in the next 5 years. I will most likely be using a Random Forest algorithm to predict overdoses in each state based on number of deaths as well as how many teens use drugs. 

I will be using Python and Random Forest because I have the most experience with these. Random Forest will also be beneficial because my dataset is rather small and I won’t run into any memory issues, which is a common disadvantage of Random Forests. 
Description of Methods

For my model, I used a random forest algorithm to predict the deaths in each state based on only the drug overdose deaths in 2020. The first time the program ran, I had an accuracy rate of about 90%. The next step is to perform hyperparameter tuning in order to get the accuracy rate higher. 

For the hyperparameter tuning, I will be adjusting the amount of data I use, as well as the random state number and number of estimators as shown below. 

I used a random forest algorithm because many prediction examples referenced online used a random forest. One of the big disadvantages of the random forest algorithm is that it can take too much memory when working with a large dataset. My data set is rather small, so I used random forest. 

After creating the random forest model, I realized that it was not working for my dataset. I did some more research and ended up creating a linear regression model for my data.  The random forest model had an accuracy of about 93% but I was struggling to include all of the data, so I used a linear regression model in Python using Sklearn. Based on the visualization of the results, the linear regression model was not as accurate but it included predictions for all states based on the 2020 drug overdose death data. 


References

Koeherson, W. (2017). Random Forest in Python. Towardsdatascience. https://towardsdatascience.com/random-forest-in-python-24d0893d51c0

Mukherjee, S., Becker, N., Weeks, W., Ferres, J. (2020). Using Internet search trends to forecast short term overdose deaths: A case study on Connecticut. IEEE Xplore. https://ieeexplore-ieee-org.mutex.gmu.edu/document/9356254

Wadekar, A. (2019). Predicting Opioid Use Disorder Using A Random Forest. IEEEXplore. https://ieeexplore-ieee-org.mutex.gmu.edu/document/8753945
