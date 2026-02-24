## Quora Question Pair

Built a Quora duplicate-question detection system to predict the probability that two questions have the same intent.

Used 404,290 question pairs and split the data into 70% train and 30% test.

Defined business constraints: high cost of misclassification, probability output required, and partial interpretability.

Evaluated models using log-loss and binary confusion matrix.

Engineered basic text features such as question length, number of words, word overlap, word share and question frequency.

Engineered advanced similarity features including common word/stopword/token ratios, first-word and last-word match, absolute and mean length difference, fuzzy matching scores and longest common substring ratio.

Extracted TF-IDF n-gram features (1-gram to 3-gram) from the combined questions.

Computed semantic features using pretrained GloVe embeddings, including Word Mover’s Distance and multiple vector distance measures (cosine, Euclidean, Manhattan, Canberra and Minkowski).

Trained and tuned Logistic Regression, Linear SVM, Random Forest and XGBoost models using sampled data due to memory constraints.

Compared models using different feature combinations (basic, advanced, TF-IDF and embedding-based distances).

Achieved the best performance with XGBoost using all feature groups (BF + AF + distance + average word vectors) with a log-loss of 0.313.
