# Toxic-word

#### For my capstone project, I plan to create a model to classify comments into toxic and non-toxic.


#### This dataset came from kaggle and was made by collecting public comments  from the Civil Comments platform. https://www.kaggle.com/competitions/jigsaw-unintended-bias-in-toxicity-classification/data

#### The text of the individual comment is found in the comment_text column. Each comment in Train has a toxicity label (target), and models should predict the target toxicity. Target >= 0.5 will be considered to be in the positive class (toxic).

The data contains new missing data. I start by checkin the balance of the dataset. There are 106,438 positive comment and 1,698,436 negative comments. So I chose a portion of negative comments and combie with all postive comments to make a balanced dataset. Now each class contains 106438 comments
![image](https://user-images.githubusercontent.com/103546558/223063629-539b2027-e1a5-476f-9af2-2327839ecf66.png)

Then I start to preprocess the data. I removed all non-alphabetic characters from each comment. I also remove the stop the stop words, lemmatize the words, and stem the words. 

I first use tradition models including logistic regression, naive bayes, random forest, and svm. The models took too long to train. I chose 0.1 of whole dataset to train. Here is the result on the test set
![image](https://user-images.githubusercontent.com/103546558/223066701-45242d1f-e7bf-4811-b109-986ab555e743.png)



I then use neural network, LSTM, and CNN. Here is the result
![image](https://user-images.githubusercontent.com/103546558/223073831-fbbd31d4-88cb-4fcd-84b3-ba6b6740f0d9.png)
![image](https://user-images.githubusercontent.com/103546558/223075810-c4aad140-3e67-4194-96cf-0bea51426917.png)


Overall, LSTM give me the best accuracy with 0.8893 and the least traning time. In the next step, I will do more preopossing and fune tuning. I will alsp try ensemble methods. Nueral network give me very high traning accuracy. Maybe booststrap is a good method to improve test accuray.
