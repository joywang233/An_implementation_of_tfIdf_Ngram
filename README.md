# An_implementation_of_tfIdf_Ngram
### Introduction 
This is an implementation of tf`idf and trigram of unstructured text data.
The dataset used here is 'million ABC news headlines', can be download from https://www.kaggle.com/therohk/million-headlines. 
A million news headlines and its published date are provided in this dataset from 2003 until 2020.

### Language and packages 
This project is implemented in Python on jupyter notebook.
The packages used here includes numpy,re, nltk, sklearn

### Purpose
The purpose of this project is to understand the top national news in Australia for the past 10 years. 
From the tf`idf, we could get insight regarding the most talked terms among the news titiles, and the implementation of Tri-gram further helped us to understand the events happended on news for the past ten years. The conclusion is quite interesting. The complete code and report can be found from the project. 

ABC News is a public news service provider in Australia. Their news service cover multiple topics including 'politics, World, Business, Analysis, Sport, Science, Health, Arts and other."(sourced from: https://www.abc.net.au/news/ )

To understand the top national topics, we would like to know which news are mostly reported by ABC. This can be achieved through counting the most frequent occured terms(term frequency) and 'tfidf'(inverted term frequency), which weight the importance of terms among a set of ducoments.

Firstly, let's take a look at the dataset.

###
`#read the csv file
My_news_tilte = pd.read_csv('abcnews-date-text.csv', sep = ',', parse_dates=[0], infer_datetime_format=True)
print(My_news_tilte.head())
My_news_tilte.info()
#[1186018 rows x 2 columns]`
