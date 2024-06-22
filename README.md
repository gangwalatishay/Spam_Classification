**Importing Libraries and Loading Data:**
Imported necessary libraries.

Loaded the dataset (spam.csv) using pd.read_csv with appropriate encoding (latin-1).

**Data Cleaning and Preprocessing**:

Removed unnecessary columns (Unnamed: 2, Unnamed: 3, Unnamed: 4).
Renamed columns (v1 to target, v2 to text).
Applied label encoding to convert target ("ham" and "spam") to numerical values (0 and 1).
Checked for and removed duplicate entries.
Analyzed basic statistics and distributions using histograms and pair plots.



**Exploratory Data Analysis (EDA)**:

Visualized class distribution using a pie chart.
Calculated and visualized statistics like number of characters, words, and sentences per message.
Created histograms and pair plots to explore relationships and distributions.

**Data Preprocessing for NLP**:

Created a function (transform_text) for text preprocessing:
Lowercasing, tokenization, removing special characters, stop words, and punctuation.
Applied stemming using Porter Stemmer.
Applied preprocessing to the text data (data['text'].apply(transform_text)).

**Visualization Using WordClouds**:

Generated word clouds for both spam and ham messages to visualize important words.

**Model Building and Evaluation**:

Used Naive Bayes classifiers (Gaussian, Multinomial, and Bernoulli) and evaluated their performance using accuracy, confusion matrix, and precision scores.
Compared Naive Bayes models with other classifiers like Logistic Regression, SVC, Decision Trees, Random Forest, AdaBoost, Bagging, Extra Trees, Gradient Boosting, and XGBoost.
Identified Multinomial Naive Bayes and Bernoulli Naive Bayes as performing best based on precision scores.
Built a Voting Classifier combining K-Nearest Neighbors, Random Forest, and Extra Trees classifiers, achieving high accuracy and precision.

**Model Improvisation**:

Explored ensemble methods like Voting Classifier and Stacking Classifier.
Opted for a Voting Classifier due to its high precision score (97%) on the test set.
Saved the final model (voting) and TF-IDF vectorizer (tfidf) using pickle for future use.
