# mindhunter
python scripts that train a variety of scikit learning models on an FBI data set of murder records (ranging from 1980 to 2014 in the US). 

#

 I realize serial killers and single count murders differ vastly when it comes to psychological factors, but I still figured it would be interesting to have a look at some real life data and find a way to predict the race of the killer based on race of the victim

 
#

I wanted to have a look for myself after having seen the tv show "Mindhunter" where a special FBI agent is convinced the perpetrator must be of black ethnicity when all his victims are black. On Kaggle.com I found a data set with 638454 rows of data on killings, containing many discernible categories. I then looked into machine learning models. There are many algorithms to choose from on scikit-learn.org. Not too much thought went into picking the algorithm, as I was trying things out. luckilly a lot of the algorithm models can be fitted in the same way. So it's little effort to try out multiple once the data is encoded.
Some models seem to compute slightly faster than others but I have yet to measure and compare their performance.
 
 #
 
 For the script on the decision tree classifier I initially encoded the race categories of victims to integers using the label encoder, but this led to there being an unwanted order in the race categories. I then swapped to one-hot-encoding instead, this did not alter the accuracy of the model, but it did deal with the random order. 
Adjusting the values of how much test and training data that got fitted into the model, barely had any effect on the accuracy of the prediction. 
I think the problem boils down to the data set being imbalanced, which can be seen scrolling down the page and having a look at some of the graphs I plotted on male/ female murderers. There's big amounts of data involving black and white perps/victims, but in comparison, very little involving natives and asians. So the model is generally going to be biased towards these two classes, resulting in poor accuracy. Some ways to change this would be to remove the races with very few counts from the test data entirely or to only take a comparable amount of data from the classes that are over-represented in comparison to those that are less represented, but I'm not sure how fair that would be (initial thought: not quite!). Still, I opted to at least try the first 'cheat' in my 4th model script and (perhaps unsurprisingly) the accuracy is ending up much higher at around 88% which seems logical when glancing over the percentages that i printed out in the final cell.
 
 #
 
 In conclusion: It seems there's about a 60% accuracy in predicting the perp based on race when using the available data in the model on race, but when making certain assumptions we can make the predictions more accurate. 


