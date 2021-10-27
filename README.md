# SentimentAnalysisCNN-Indonesia (Using Jupyter)
Given a sample of data in the form of online news from one of the online news sites in Indonesia (CNN Indonesian)

1. Preprocessing data methods:
- Labeling            : Translator library to translate bahasa to english, then labeling using TextBlob library to find polarity (neutral, negative, and positive                           emotion)
                          
- Case Folding        : Using lower() method
- Remove Punctuation  : Using ...str.replace('[{}]'.format(string.punctuation), '')
- Remove New Line     : Using ...replace(r'\n',' ', regex=True)
- Stop Word           : Using ...apply(lambda x: ' '.join([word for word in x.split() if word not in (stop_words)]))

2. Library for cleansing data in sentiment analysis<br>
I use TextBlob library to find polarity of newspaper headline (title), before that I must translate newspaper headline (bahasa) to english because TextBlob library can only recognize english and there is still no TextBlob Adapter for Indonesian. Then, polarity is used to see how positive or negative a text is (neutral = 0, negatif < 0, and positif > 0). After all headlines have been classified, the polarity of all headlines will be displayed as an average, and the label 'Neutral', 'Positive' or 'Negative' corresponds to the mean of the polarity of all headlines.

3. Algoritm to analyze sentiment analysis<br>
I use decision tree model, because compared to other algorithms decision trees requires less effort for data preparation during pre-processing, decision tree model is often used as a method to predict the presidential election from news data and has good accuracy, and decision tree model is very intuitive and easy to explain to technical teams as well as stakeholders.

4. Create word cloud<br>
The last, I create word cloud, it is a simple visualisation of data, in which words are shown in varying sizes depending on how often they appear in my text/data.

