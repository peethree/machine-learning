# mindhunter
a script that trains a Decision Tree Classifier on a dataset of murder records

#

 I wanted to go over a murder database after having seen the tv show "Mindhunter" where an FBI agent is convinced the perpetrator must be of black ethnicity when all his victims are black.

#

 I fully realize serial killers and single count murders differ vastly when it comes to the psychology of the murderer involved, but I still thought it interesting enough to have a look at some real life data and find a way to predict the race of the killer based on race of the victim
 
 #
 
 Initially I encoded the race categories of victims to integers, but this led to there being an unwanted order in the race categories. I then swapped to one-hot-encoding instead. I later found out that label encoding is only really useful while having two categories, which is not the case here.
Sadly enough, however, trying different types of encoding didn't help the accuracy of the prediction much. After some reflection, using a classifier tree for the data that I chose to use for the model was never going to perform well since the data itself is very imbalanced. There's a ton of data involving black and white perps and victims, but in comparison very little involving natives or asians. So the model is always going to be biased towards these two classes.
 
 #
 
 In conclusion: using this dataset and the model I opted for, it seems there's about a 60% accuracy in predicting the perp based on race. 


