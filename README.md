# Sentiment-analysis-on-Peers-Reviews

Capstone Project on a  Spanish dataset.

Dataset link: https://archive.ics.uci.edu/ml/datasets/Paper+Reviews

The data set consists of paper reviews sent to an international conference mostly in Spanish (some are in English). It has a total of N = 405 instances.

 ## Project Delivery Phase 1:

For now, I'm mostly discovering my data.
I was able to extract the text data for preprocessing purposes.
I will be focusing only on the Spanish texts.

Some preprocessing steps I did:
-LowerCase
-Tokenization
-Remove stop words
-Remove punctuation
-Lemmatization

My first approach was with NLTK, but I had a problem with lemmatization. NLTK does not handle very well, lemmatization on Spanish words.

I finally used spaCy, which seems to be better for Spanish lemmatization.

The steps to lemmatize with spaCy :

-pip install sapcy_spanish_lemmatizer
-import spacy
-import spacy_spanish_lemmatizer
-from spacy.lang.es.stop_words import STOP_WORDS
- Pipeline package (https://spacy.io/usage/models). Run the code below
python -m spacy download es_core_news_sm
import es_core_news_sm
nlp = es_core_news_sm.load()

### First modifications
I created a new notebook called:" Preliminary_decisions"

Before running this notebook, I have to first run the "review_GitHub" notebook, 2 CSV files will be created and later used in the " Preliminary_decisions" notebook.

With " Preliminary_decisions" I'm trying to predict if a paper will be rejected or accepted for publication. 
I merged 2 data frames (created from the 2 CSV files) to create a new data frame.
I trained the model using "train_test_split" from Sklearn
For vectorization and Feature Engineering, I used (TF-IDF)
For model prediction, I calculated accuracy_score, precision_score, recall_score
I used "classification_report()" to build a text report showing the main classification metrics.

#### Last Notification
The Notebooks have to be run in this order

1- review_GitHub.ipynb 
2- Spanish_sentiment&Preliminary_decisions.ipynb
3- Reviews_sentiments.ipynb
4- English_translation.ipynb
5- Sentiment_on_English_Reviews.ipynb
6- Classifier_models.ipynb


I used IBM translator to translate the reviews from Spanish to English. For this you will need your own "Apikey" & "url"