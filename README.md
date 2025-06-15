
# Flipkart Product Review Sentiment Analysis using Deep Learning

## 🧾 Overview

This project uses a **Deep Learning-based NLP model** to analyze customer reviews from Flipkart and classify them into positive or negative sentiments. It utilizes a dataset of Flipkart reviews to classify each review as either positive or negative. The modeling involved using a Decision Tree Classifier initially and then improving the performance by employing a Random Forest Classifier combined with techniques to handle class imbalance, ultimately achieving good performance in sentiment classification.


---

## 🧠 Business Understanding

The primary stakeholders for this project would likely be Flipkart and its sellers. The business problem being addressed is the need to quickly and efficiently gauge customer satisfaction with products. Manually sifting through thousands of reviews to understand sentiment is time-consuming and impractical. By automating sentiment analysis, businesses can:
- Identifying product performance and customer satisfaction
- Enhancing user experience
- Flagging negative trends early
- Improving recommendations and marketing

Manual review analysis is infeasible at scale — hence, an automated sentiment classifier is highly valuable.

---

## 📊 Data Understanding
The data used in this analysis consists of Flipkart product reviews consisting of 9976 reviews with 2 attributes. The dataset includes the text of the review and a rating associated with it. A key characteristic of this dataset is its class imbalance, where there are significantly more positive reviews than negative ones.

The dataset includes:
- Customer-written **review texts**
- Corresponding **star ratings** (used to infer sentiment)

### Preprocessing:
- Text normalization (lowercasing, punctuation removal)
- Stopword removal
- Tokenization and vectorization (TF-IDF)
- Label creation: binary sentiment (`positive` vs `negative`) from ratings

---
## Visualizations included in the analysis
- A bar plot showing the distribution of positive and negative sentiments. This clearly illustrated the class imbalance issue.
![image](https://github.com/user-attachments/assets/e20468a5-e66a-4870-a90d-2721b7680da4)
 
- A word cloud visualizing the most frequent words in positive reviews, providing insight into common positive feedback themes.
  ![image](https://github.com/user-attachments/assets/e336d3c4-6177-469a-afeb-0c019efe95b5)


## 🤖 Modelling & Evaluation
- **Decision Tree Classifier: -**  Initially, a Decision Tree Classifier was used for sentiment classification. The evaluation of this model showed reasonable overall accuracy but struggled with the minority class (negative reviews), as evidenced by lower precision and recall for that class.
- **SMOTE (Synthetic Minority Over-sampling Technique): -** Applied to the training data to create synthetic samples of the minority (negative) class, balancing the dataset for training.
class_weight='balanced': Used with the Random Forest model to give more importance to the minority class during training.
Stratified Train-Test Split: Ensured that the proportion of positive and negative reviews was maintained in both the training and testing sets.
The evaluation of the Random Forest model with these improvements showed:


### Evaluation:
- Accuracy, Precision, Recall, F1-Score
- Confusion Matrix

---

## 📌 Conclusion
The **Random Forest Classifier with class imbalance handling performed significantly better** than the initial Decision Tree model. While the Decision Tree had an accuracy of around 0.85, it struggled with identifying negative reviews (recall ~0.56, F1-score ~0.58). The improved **Random Forest model** achieved an accuracy of **0.87**, but more importantly, dramatically increased the **recall for negative reviews to 0.72** and **the F1-score for negative reviews to 0.67.** This shows the Random Forest model is much more effective at capturing negative feedback, providing a more balanced and useful sentiment analysis for stakeholders.
To improve the model performance we can explore more advanced text processing techniques (e.g., n-grams, handling negation, using pre-trained word embeddings).

---

## ✅ Tech Stack

- Python
- NLTK, Scikit-learn
- Matplotlib, Seaborn

---
