# An_implementation_of_tfIdf_Ngram
### Introduction 
This is an implementation of tf`idf and trigram of unstructured text data.
The dataset used here is 'million ABC news headlines', can be download from https://www.kaggle.com/therohk/million-headlines. 
A million news headlines and its published date are provided in this dataset from 2003 until 2020.

### Language and packages 
This project is implemented in Python on jupyter notebook.
The packages used here:


```
import numpy as np
import re #for tokenization
import nltk #nlp library for stop-words
import string #for punctuation (in case there's any)
from sklearn.feature_extraction.text import TfidfVectorizer, CountVectorizer
```


### Purpose
The purpose of this project is to understand the top national news in Australia for the past 10 years. 
From the tf`idf, we could get insight regarding the most talked terms among the news titiles, and the implementation of Tri-gram further helped us to understand the events happended on news for the past ten years. The conclusion is quite interesting. The complete code and report can be found from the project. 

ABC News is a public news service provider in Australia. Their news service cover multiple topics including 'politics, World, Business, Analysis, Sport, Science, Health, Arts and other."(sourced from: https://www.abc.net.au/news/ )

To understand the top national topics, we would like to know which news are mostly reported by ABC. This can be achieved through counting the most frequent occured terms(term frequency) and 'tfidf'(inverted term frequency), which weight the importance of terms among a set of ducoments.

Firstly, let's take a look at the dataset.

### Findings

-'Same sex marriage' is a high ranked topic. This is because Australia legalised same-sex marriage in December 2017, which has caused a heated discussion among the nation.

-'Social news' is also a widely discussed topic, this can be seen from the high ranked terms such as 'not guilty to','man killed in','being hit by','police','ctash','murder' etc.

-'Business news' is another hot topic within past decade, indicated by high ranked term 'the consumer quarter', 'market analysis', 'finance with alan' etc.

However, high ranked tri-gram such as 'one plus one', 'the drum ', 'Tas country hour', 'National press club ' are the names of TV/broadcast programmes owned by ABC News. These grams are actually not adding much value to the reader's insight. To get rid of these less useful terms, a customized stop words list can be added at pre-processing stage later.

###Future work

-Though tri-gram works well on our sample dataset, it has greatly increased the dimension compare with single terms. For 67571 news_titles, the dimension of tri-gram went from 24k to 273k. It is unrealistic to apply tri-gram on the whole dataset.

-To further reduce the dimension and make the topics clear, a topic model would be a better option, here LDA (Latent Dirichlet allocation) will be choose as our future approach.
