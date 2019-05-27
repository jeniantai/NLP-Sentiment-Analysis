# Sentiment Analysis on 10-Ks

## Introduction and Goal
Comparing to the prohibitvely expensive data purchased from data vendors and corpoations, unstructured text data is the most abundant, unused (and free) alternative resources available for systematic alpha searching. While news headlines and analyst estimates were the obvious drivers of market movements, so too can the general tone of the management in the earning reports. Starting with low frequency data, this project is my first attempt to discern negative or positive sentiments in financial statements using NLP tools. The goal is to explore and unlock the hidden value of text data, and ultimately creating a decision-making engine that more closely mimick human performance and predicting the general trend of companies/sectors.

### Hypothesis
Management Discussion and Analysis is ignored by financial news reporters, and it is not carefully read by many analysts.  However, there is a wealth of critical information in there - more prudent outlook governed by regulators, highlights of operational metrics & KPIs, and critical accounting policies & estimates etc. There is value to be extracted from the information.

### Model
We use two ways to convert the text data into numbers - 1) CountVectorizer, which just counts the word frequencies; and 2) TfidfVectorizer, which penalizes words appear more frequently. For this project, we encountered a lot of standized wordings, and we don't want them.  Therefore, Tfidf is a better approach for search query relevance. We implemented both for comparison.

### Result and Conclusion
We found that there was a positive correlation between return and the similarities scores over the time for our e-commerce stocks, especially when the signal was confirmed with high similarity scores.  However, the alpha wasn't consistent across sentiments and levels. Moreover the autocorrelation/stability of the factor wasn't great. 

Our next step is to expand the research to other sectors, other countries, and we should consider 2-gram and 3-gram, tune the right parameters for the model.

Data Source: https://www.sec.gov
