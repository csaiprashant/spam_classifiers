# Build various spam classifiers using sklearn and NLTK

In this project, we build various spam classifiers using sklearn and NLTK. The metric to compare the performance of these classifiers is AUC score.

The table shown below lists the different classifier - feature combinations used and their performance.

| Model | Base Classifier | Features | AUC Score |
|---|---|---|---|
| 1 | Multinomial Naive Bayes (alpha=0.1) | Count Vectorizer (default params)  | 0.972 |
| 2 | Multinomial Naive Bayes (alpha=0.1) | TF-IDF Vectorizer (min_df=3)  | 0.942 |
| 3 | Support Vector Machine (C=10000) | TF-IDF Vectorizer (min_df=5) + length of text  | 0.958 |
| 4 | Logistic Regression (C=100) | TF-IDF Vectorizer (min_df=5, ngram_range=[1, 3]) + length of text + number of digits per document | 0.968 |
| 5 | Logistic Regression (C=100) | TF-IDF Vectorizer (min_df=5, ngram_range=[2, 5]) + length of text + number of digits per document + number of non-word characters | 0.979 |

Legend:
* alpha - smoothing parameter
* C - regularaization parameter
* min_df - minimum document frequency
* ngram_range - word n-grams to be used (unigrams, bigrams, trigrams, 4-grams, 5-grams)

Refer [sklearn](https://scikit-learn.org/stable/documentation.html), [NLTK](https://www.nltk.org/) documentation for more details.
