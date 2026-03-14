# SMS Spam Classifier: NLP & Ensemble Learning

## 🚀 Project Overview
This project focuses on building a robust SMS spam detection system. Using a dataset of over 5,000 messages, I implemented an end-to-end Machine Learning pipeline—from raw text cleaning to advanced model stacking—to accurately distinguish between "Ham" (legitimate) and "Spam" messages.

## 🛠️ Technical Workflow
The project is divided into four critical stages:

### 1. Data Cleaning & Preparation
- Handled missing values and removed duplicate entries.
- Converted target labels into binary format using **Label Encoding**.
- Dropped irrelevant columns to streamline the dataset.

### 2. Exploratory Data Analysis (EDA)
- **Feature Engineering:** Created new features for the number of characters, words, and sentences in each message.
- **Statistical Analysis:** Visualized how these features varied across classes, revealing that spam messages typically contain significantly more characters and words.
- **Correlation Mapping:** Used heatmaps to identify relationships between engineered features.

### 3. Advanced Text Preprocessing
Standardized raw text for the machine learning models:
- Lowercasing and Tokenization.
- Removal of special characters, punctuation, and stopwords.
- Applied **Porter Stemming** to reduce words to their root forms.
- **Vectorization:** Compared Bag of Words (CountVectorizer) and **TF-IDF** (Term Frequency-Inverse Document Frequency).

### 4. Model Building & Stacking
- Evaluated multiple baseline models including **Logistic Regression** **Naive Bayes** (Gaussian, Multinomial, Bernoulli).
- Integrated advanced classifiers: **Random Forest**, **Extra Trees**
- **Final Architecture:** Implemented a **Stacking Classifier** to combine the strengths of the top-performing models, significantly enhancing overall performance.

## 📊 Key Results & Conclusions
- **Best Model:** The Stacking Ensemble method outperformed individual baseline classifiers.
- **Performance Focus:** Prioritized **Precision** and **F1-score** over simple accuracy to ensure legitimate messages are rarely misclassified as spam.
- **Key Insight:** Character count is a strong predictor of spam, as spam messages are often longer and more descriptive.

## 💻 Tech Stack
- **Language:** Python
- **Libraries:** NumPy, Pandas, Scikit-learn, NLTK, Matplotlib, Seaborn
