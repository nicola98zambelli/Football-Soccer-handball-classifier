# **Football (Soccer) handball classifier**
### *Introduction*
Technology in football is becoming more and more important and the Video Assistant Referee (VAR) is one of the most recent and significant technological innovations in the world of football.
This small project tries to implement a machine learning algorithm for the classification / identification of handballs in football (soccer) in order to be able to help the referee to make a decision and decrease the waiting times of the match.
### *Training/Validation Phase*
The first phase was the collection of images of game action and handballs. In turn, these are divided into train data, used to train the algorithm and validation, and test data, to evaluate its performance, with a ratio of about 70 30. To arrive at the final model, I used the keras software and the library it makes available, TensorFlow, in particular I used a learning rate equal to 10e-5, a crossvalidation batch size equal to 16 (k about 7), at least 200 epochs were made and then the learning curves started to diverge (ie the test loss started to grow). The validation performance is good but not great with a hand and no hand foul accuracy of 75% and 94% respectively. the reason is very simple to explain: the data collected are too few (unfortunately if you look for images of handballs on search engines after a while the images are always the same and should not be included in the dataset as they are correlated with other observations, this is the big limitation of the work because the collected handball images are only 159, the ideal would be at least 5000).

![Image](https://user-images.githubusercontent.com/98172442/224316075-3f945934-22cd-4fc4-b41f-061e8293a03d.PNG) 
![Image](https://user-images.githubusercontent.com/98172442/224316100-48c94776-e70c-467e-a639-a52498ae8ab4.PNG)
### *Test Phase*
Once the described model was obtained, I moved on to the test phase, which shows very excellent performances on the 46 and 42 images left for the test of hand and non hand fouls respectively. The Confusion Matrix shows an accuracy of 95% for handballs and 78% for fouls, overturning the validation results. The latter is not a good sign as the data may be distorted. This is solved by adding date which I don't have.
![Image](https://user-images.githubusercontent.com/98172442/224317182-63962651-ca28-4f2b-804a-1e9f119e834f.PNG) ![Image](https://user-images.githubusercontent.com/98172442/224317219-b1e33bbb-efc3-405a-bc04-f45ff4f4a315.PNG)
### *Conclusion*
In conclusion this work can be a good starting point for identifying handballs in soccer or to help the referee make decisions in a short time, for example given a small video this could be broken up into 60 frames per second and evaluate the frame with the highest probability of handball, helping to understand immediately if a handball has occurred which is a necessary but not sufficient condition for there to be a handball, due to involuntariness, distance, etc. ...
### *TO USE*
To use the model, just download the folder with the script and the model and change the path to the image you want to classify.
