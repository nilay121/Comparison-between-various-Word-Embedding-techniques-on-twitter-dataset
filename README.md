# Comparison-between-various-Word-Embedding-techniques-on-twitter-dataset

In this notebook I have made a comparison between the various word embedding techniques i.e Simple Embedding Layer, Glove Vectors, Word2Vec. For this comparison I hvae used the twitter dataset from kaggle having 162980 records. The target column contains three classes namely "poisitive", "negative" and "normal", so we can see that it is a multiclass classification problem. I have written a small function to clean the tweets by tokenizing the text, converting all the words to lower case so that there isn't any difference between "hello" and "HELLO" for the model, then lemmatizing or stemming the tokens.
<h3> Embedding layer</h3>
First we one hot encoded the cleaned tweets then added padding to make the size of all the tokens to be same, the padded list of tokens are then passed to the embedding layer of neural Network for training.<br>
<img src="https://github.com/nilay121/Comparison-between-various-Word-Embedding-techniques-on-twitter-dataset/blob/main/embedding%20layer%20.png" height="300px" width="600px"><br>
The figure above shows the model summary, as you can see we have used lots of dropout layer to reduce the overfitting of the model. With this architecture we have achieved an accuracy of about 87% on the validation set, though the model was trained for only 5 epochs still the accuracy obtained was quite satisfying.<br>
I have also used CNN pooling layers along with the embedding layer to see if the presence of pooling layers somehow impact the accuracy, though I didn't see any considerable amount of accuracy increment, but that might be due to the less number of epochs.<br>
<h3> Glove Vectors </h3>
For using Glove, I have downloaded the glove text file from the Standford website, the txt file contains key value pairs, where the word is represented as the key and the 100/200/300 dimensional vector is as the value. I created a weight matrix using the glove vectors, by weight matrix we mean to say that all the one hot encoded value of the words that we obtained earlier during pre-processing for simple embedding layer will be replaced by 100d glove vector. This weight matrix is then passed to the embedding layer of neural network as weight parameter.<br>
<img src="https://github.com/nilay121/Comparison-between-various-Word-Embedding-techniques-on-twitter-dataset/blob/main/glove.png" height="300px" width="600px"><br>
<h3> Word2Vec </h3>
In order to use word to vec we are using the Gensim library which can be simple installed by typing <br>

```bash
pip install gensim
```
uhuihihoh



