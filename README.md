# LSTM-recurrent-neural-network-arquitecture
In this project I will build a LSTM arquitecture to identify basic emotions in amazon products reviews both positive(happy, excited, etc.) and negative (sad, worried, etc.).
# Loading the data
The dataset I will use is the amazon product review that is stored on the tensorflow database.

Then I will convert to a pandas dataframe.
Since the data is about text, machine learning models understand numberical features, I need to convert the review columns into numerical values.

In this application,I'm going to use the Tokenizer class from Keras preprocessing

The tokenizer will convert each word in a sentence into integer tokens/IDs based on the frequency of the word appearing in the corpus.

I will convert our feature column and label into a set of lists as that’s how our Tokenizer wants our data. To apply the Tokenizer to the corpus, I will split the dataset into training and testing sets as the tokenizer only needs to be fit on the training set and not on the test set.

Now I going to start building the model, since the goal is to build a LSTM arquitecture, the structure of the model is as follow:

1.  The Keras embedding layer will be trained with the word that we get from the reviews, initializing with random weights and is defined as the first hidden layers of the network
2.   EThe LSTM layer are going to learn what emotion are represented int the words if is negative or positive.
3.   The last one is the Dense layer which is the fully connected layer that ensure that the model learn well and improve his accuracy.

# **Performance analysis**

after trainning the model with 5 epochs and 128 batches I got a loss of 43% and a accuracy of 82.1% on the training side and a loss of 45%  and accuracy of 83.3% in the validation data, which is a great indicator of good performance

# **Conclusion**

That's it for the project, in this case I better understand now the arquitecture of LSTM models and the advantage tha this have over sequencial data, this model need more hiper-parameter tunning and testing with real-life examples from customer reviews, also we can also compare the this model, with other NLP tools like transformer for example, but this will be in a future project. you can download the H5 file in the GitHub repository to use the pre-trained model to futher analysis.
