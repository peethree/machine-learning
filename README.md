# mindhunter
python scripts that train a variety of scikit learning models on an FBI data set of murder records (ranging from 1980 to 2014 in the US). 

#

 Serial killers and single count murders differ vastly when it comes to psychological factors, but I still figured it would be interesting to have a look at some real life data and find a way to predict the race of the killer based on race of the victim
 
#

After having seen the tv show "Mindhunter", I wanted to have a look for myself if -- the character -- special FBI agent Ford's notion that the perpetrator must be of black ethnicity when all his victims are black, is based on anything substantial. On Kaggle.com I found a data set with 638454 rows of data on killings that happened over multiple decades in the US, containing many discernible categories. I then looked into machine learning models. There are many algorithms to choose from on scikit-learn.org. Luckilly, the algorithm models seem to be fitted in the same way. So it's little effort to try out multiple once the data is encoded.
 
 #
 
I first checked the data so see if there were any null values in the data, but hats off to the FBI for having a clean dataset. Not every murder is solved, however. Leading to the value of, let's say, 'perpetrator race' to be unknown in those cases. Initially I took the data of victim race and perpetrator race as is and fitted it into some linear machine learning models. The result was mostly the same: roughly 60% prediction accuracy, not very impressive. Adjusting the values of how much test and training data that got fitted into the model, barely had any effect on the accuracy of the prediction.
To get a good overview of the data (which in hindsight should have been done before anything else), I plotted the murders committed by men and women, specifically looking at race, and the graphs show the victim counts are extremely imbalanced. Many white/black victims and perps, few Native/Alaskan and Asian/pacific victim/perps in comparison. So the model is generally going to be biased in favor of the dominant classes, resulting in poor accuracy. Some ways to circumvent this would be to remove the races with very few counts from the test data entirely or to only take a comparable amount of data from the classes that are over-represented to those that are less represented. That is what I did next. 
Taking only the two most represented races (white and black) leads to a big increase in accuracy, the result being around 88%. Even though the victim count of black and white victims is fairly similar. I tried balancing them even further and had another model do predictions. This did not increase the accuracy over 88% though.
I then revisited the less represented races and included them in the predictions. This time only ommitting the "unknowns", but also balancing the data around the race with the smallest victim count. The outcome was 72% prediction accuracy, approximately a 12% increase in accuracy compared to the predictions of models involving every bit of data from the fbi murder statistics. 
Between different models i toy with differing test- and trainingdata sizes. This might alter the accuracy and duration it takes for the model to make the predictions. If my goal was to figure out which algorithm was the fastest or had the best performance for this problem, I would have kept the circumstances as equal as possible between the models. 
 
 #

 ![graph]([http://url/to/img.png](https://i.imgur.com/0HCmiRv.png)https://i.imgur.com/0HCmiRv.png)
 
 


