# Political Bias Classifier for News

The notebook `pol_views_classifier.ipynb` classifies English-language news articles by political bias: **left / center / right**.

## Data
Kaggle: https://www.kaggle.com/datasets/gandpablo/news-articles-for-political-bias-classification. The `leaning-left` and `leaning-right` labels are merged into `left` and `right`. Train/test split: 80/20, stratified.

## Models
- **TF-IDF / Doc2Vec / Word2Vec** + Logistic Regression and LinearSVC (after spaCy lemmatization)
- **BiLSTM** and **TextCNN** (Keras)
- **DistilBERT**, fine-tuned on this dataset
- **DistilBART-MNLI**: zero-shot and few-shot (with descriptive labels)

For each model, the notebook prints a classification report and a confusion matrix, plus the top words that most influence each class.