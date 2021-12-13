# Data science fundamental project: 
# Tweet sentiment Analysis during COVID-19

## Introduction 

This project was chosen for several reasons, firstly to understand the overall feeling on the global situation of COVID 19 on the Twitter network. In addition, this project allowed us to have a first approach to text processing in machine learning. Especially the preprocessing, cleaning, and tokenization part. Finally, thanks to this project, we were able to work with advanced deep learning models to create a model capable of classifying tweets into three classes: positive, neutral, and negative.  
**The main objective of this project is to create a classifier on sentiment by giving a tweet on the subject of covid.**

## Selection of Data 

The data used are tweets extracted from the Twitter platform. They were extracted at the beginning of the covid 19 pandemic. These tweets have been selected by their hashtags such as #covid19 or #covid. These tweets were then annotated to classify them into 5 different classes: 'Extremely Negative' 'Extremely Positive' 'Negative' 'Neutral' 'Positive'. To simplify our analysis and the simplicity of our model, we decided in the preprocessing phase to modify these 5 classes into only 3: 'Negative' 'Neutral' 'Positive' thus reducing the possibilities of choice for our model.
In addition, we had to clean up the tweets so that they could be given to a learning system. To do this we will remove all special characters, https links, and we will use a library that contains "stopwords" which are words that do not provide information, for example: 'the' 'a' 'he' ect. We can then remove them from the tweets.  

The data are from Twitter, the maximum length for text in this network is 280 characters. Another limitation of this dataset is that it only contains tweets in English, and therefore mostly from English-speaking countries. It is therefore not possible to be sure of the generalization of the results to non-English speaking countries. 

## Methods

In order to realise our classification, we have realised a deep neural network using the Tensorflow library. The network is composed of many layers including embedding layers, Bidirectional LSTM, dense layers and drop out layers. 
In addition, in order to enter the previously cleaned data we had to tokenize it. This allows us to transform each word into a vector of numbers 

## Results 

After training this model performs well in classifying tweets into 3 classes: . Indeed we obtain an overall accuracy of 84% of good classification. 
Thanks to this confusion matrix we have a visual of this good performance 

We notice that for example the model predicts 1366 negative times and the result is really negative. On the other hand knowing the class 0, it predicted 215 times the class 2 (Positive)


## Discussion

In the cleaning part of the project, we removed the stopwords which are supposed not to contain information. However in the list of stopword we can see that there are verbs and theses in a sentences could set the tone and the direction of the tweet, removing them could also lead to a loss of information.

Also, it is important to remember that when doing sentiment analysis, the analysis is subject to the culture and the opinion of the annotator. Then the results are biais by this annotator. Covid might be a negative sentiment for some but a good sentiment for other if talking about the medical discoveries behind it for example. 

Our model can now analyze the general feeling on Covid in the English-speaking countries. When can now analyze how the feeling on covid has evolve through time, but also see the reaction of the population on restrictions. This kind of analysis would require a lot a computer power since many tweet are generated every day and an analysis on a month would mean the analysis of 1,5 billion tweets. 

## Summary

To analyze text we must follow some steps that are essential :
1. Analyze the data to avoid being biaised and make sure that the dataset is balanced.
2. Clean the data (remove stop word).
3. Tokenize the text
4. Create your model
5. Fit the model
6. Analyze performances
