# Exploring-Tinder-Message-Data-with-NLP
<b>Author:</b> Avonlea Fisher

<b>Blog Post:</b> [Diving into my Tinder Dat(e)a](https://towardsdatascience.com/diving-into-my-tinder-dat-e-a-a508269b8d10), published in [Towards Data Science](https://towardsdatascience.com/)
## Introduction
The contents of this repository explore message data from my Tinder account with Natural Language Processing. Users can request a copy of their personal data, which is made available to them via e-mail in a JSON format, using the [Download my Data](https://www.help.tinder.com/hc/en-us/articles/115005626726-How-do-I-request-a-copy-of-my-personal-data-) tool. The JSON file used in this analysis has been excluded from the repository due to the data's personal nature. 

## Methods
A list of message strings was created from the data, cleaned, and converted into a list of words that excluded stopwords. This list was used to create a that visualized the individual words that occured most frequently in the message corpus:
<img src ='https://github.com/AvonleaFisher/Exploring-Tinder-Message-Data-with-NLP/blob/main/Images/message_wordcloud.png' width="600" height="600" alt="Wordcloud"></a>

A function to obtain the top 40 most frequent bigrams and their frequency values was created with methods from the [NLTK Collocations](http://www.nltk.org/howto/collocations.html) package. These bigram-frequency pairings were added to a dictionary and visualized in a Plotly Express barplot: 
<img src ='https://github.com/AvonleaFisher/Exploring-Tinder-Message-Data-with-NLP/blob/main/Images/bigrams.png' width="1000" height="600" alt="Bigrams"></a>

Another barplot visualized the sum of the messages' sentiment scores for each class in the [VADER](https://github.com/nltk/nltk/blob/develop/nltk/sentiment/vader.py#L441) algorithm. Scores were calculated for each message and appended to lists for each sentiment category. The sum of values in these lists were plotted to explore the overall distribution of sentiments in the messages. The plot suggests that 'neutral' was the dominant sentiment of the messages:
<img src ='https://github.com/AvonleaFisher/Exploring-Tinder-Message-Data-with-NLP/blob/main/Images/sentiment.png' width="1000" height="600" alt="Sentiment"></a>

## Limitations and Next Steps
*  Tinder's Download my Data tool also provides access to information about the time that messages were sent and the count of app opens by date. A future analysis could explore temporal trends in usage of the app and/or message content. 
* As more message data becomes available in the future, this corpus may be suitable for a message classification task (e.g., identifying messages that lead up to an in-person meeting).

## Relevant Documentation

* [WordCloud for Python](https://amueller.github.io/word_cloud/#)
* [Natural Language Toolkit (NLTK)](https://www.nltk.org/)
* [vaderSentiment](https://pypi.org/project/vaderSentiment/)
* [Bar chart with Plotly Express](https://plotly.com/python/bar-charts/)

## Further Information and Resources

Please feel free to contact me at [fisheravonlea@gmail.com](mailto:fisheravonlea@gmail.com) or via my [LinkedIn profile](https://www.linkedin.com/in/avonlea-fisher/) with any comments, suggestions or inquiries regarding this project.
