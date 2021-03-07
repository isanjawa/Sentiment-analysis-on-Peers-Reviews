# Sentiment-analysis-on-Peers-Reviews

Capstone Project on a  Spanish dataset.

Dataset link: https://archive.ics.uci.edu/ml/datasets/Paper+Reviews

The data set consists of paper reviews sent to an international conference mostly in Spanish (some are in English). It has a total of N = 405 instances.

 ###Project Delivery Phase 1:

For now, I'm mostly discovering my data.
I was able to extract the text data for preprocessing purpose.
I will be focusing only on the spanish texts.

Some preprocessing steps I did:
-LowerCase
-Tokenization
-Remove stop words
-Remove punctuation
-Lemmatization

My first approach was with NLTK, but I had problem with lemmatization. NLTK does not handle very well, lemmatization on spanish words.

I finally used spaCy, which seems to be better for spanish lemmatization.

The steps to lemmatize with spaCy :

-pip install sapcy_spanish_lemmatizer
-import spacy
-import spacy_spanish_lemmatizer
-from spacy.lang.es.stop_words import STOP_WORDS
- Pipeline package (https://spacy.io/usage/models). Run the code below
python -m spacy download es_core_news_sm
import es_core_news_sm
nlp = es_core_news_sm.load()
