# mindhunter
scripts that train a variety of scikit learning models on a dataset of murder records

#

 I wanted to go over a murder data set after having seen the tv show "Mindhunter" where an FBI agent is convinced the perpetrator must be of black ethnicity when all his victims are black.

#

 I realize serial killers and single count murders differ vastly when it comes to psychological factors, but I still figured it would be interesting to have a look at some real life data and find a way to predict the race of the killer based on race of the victim
 
 #
 
 For the script on the decision tree classifier I initially encoded the race categories of victims to integers, but this led to there being an unwanted order in the race categories. I then swapped to one-hot-encoding instead, this did not alter the accuracy, but it did deal with the random order. 
Adjusting the test and train data when using all the available data in the set has barely any effect on the accuracy of the prediction. 
The problem boils down to the data set being imbalanced. There's a ton of data involving black and white perps and victims, but in comparison very little involving natives or asians. So the model is always going to be biased towards these two classes, resulting in poor accuracy. One way to change this would be to remove the races with very few counts from the test data entirely and just focus on black and white, but I'm not sure how fair that would be. Still, I gave it a shot in my 4th attempt and unsurprisingly the prediction accuracy is ending up much higher at around 88%
 
 #
 
 In conclusion: It seems there's about a 60% accuracy in predicting the perp based on race when using all the data in the model, but when 'cheating' (making assumptions) we can make the predictions more accurate. 


