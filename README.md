# mindhunter
scripts that train a variety of learning models on a dataset of murder records

#

 I wanted to go over a murder data set after having seen the tv show "Mindhunter" where an FBI agent is convinced the perpetrator must be of black ethnicity when all his victims are black.

#

 I fully realize serial killers and single count murders differ vastly when it comes to the psychology of the murderer involved, but I still thought it interesting enough to have a look at some real life data and find a way to predict the race of the killer based on race of the victim
 
 #
 
 For the script on the decision tree classifier I initially encoded the race categories of victims to integers, but this led to there being an unwanted order in the race categories. I then swapped to one-hot-encoding instead, this did not alter the accuracy, but it deals with the random order. Label encoding appears to be useful while having two categories, which is not the case here.
No matter what I do to tinker with the test and train data, the accuracy remains the same. The problem boils down to the data set being imbalanced. There's a ton of data involving black and white perps and victims, but in comparison very little involving natives or asians. So the model is always going to be biased towards these two classes, resulting in poor accuracy. One way to change this would be to remove the races with fewest counts from the test data entirely and just focus on black and white, but I'm not sure how fair that would be.
 
 #
 
 In conclusion: using this dataset and the models I opted for, it seems there's about a 60% accuracy in predicting the perp based on race. 


