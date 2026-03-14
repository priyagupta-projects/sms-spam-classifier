**SMS Spam Classifier: NLP & Ensemble Learning**

**Project Overview**
This project focuses on building a high-precision SMS spam detection system. Using a dataset of over 5,000 messages, I implemented an end-to-end Machine Learning pipeline—from raw text cleaning to advanced Stacking Ensembles—to accurately distinguish between "Ham" (legitimate) and "Spam" messages.

**Technical Workflow**
**1. Data Cleaning & Handling Imbalance**
*Imbalance Handling*: Utilized Class Weights and SMOTE (Synthetic Minority Over-sampling Technique) to ensure the model effectively identifies the minority (Spam) class without bias.

*Data Integrity*: Handled missing values and removed duplicate entries to ensure high training quality.

**2. Exploratory Data Analysis (EDA) & Feature Engineering**
*Engineered Features:* Constructed structural columns: num_characters, num_words, and num_sentences.

*Key Insight:* Statistical analysis revealed that while spam messages are generally longer, incorporating these features yielded marginal improvements in the final model compared to semantic text patterns.

**3. Advanced Text Preprocessing**
Standardized raw text for machine learning readiness:

*Cleaning:* Lowercasing, Tokenization, and removal of special characters and stopwords.

*Stemming:* Applied the Porter Stemmer to reduce words to their root forms.

*Vectorization:* Used TF-IDF (Term Frequency-Inverse Document Frequency) to convert text into a high-dimensional sparse matrix.

**4. Model Building & Hyperparameter Tuning**
*Optimization:* Used RandomizedSearchCV to conduct an exhaustive search for the best hyperparameters across all models.

*Baseline Models:* Evaluated Logistic Regression, Naive Bayes, SVM, and Random Forest.

**5. Final Architecture: Ensemble & Stacking**
*The Solution:* Achieved the best performance through a Stacking Classifier and a Voting Ensemble.

*Strategy:* By combining the strengths of top-performing models (including Extra Trees, Naive Bayes, and Random Forest) through a meta-learner, I significantly enhanced the model's reliability.

**Final Performance Results**
Given the real-world application, I prioritized Precision to ensure legitimate messages are not incorrectly blocked.

**Final Precision:** 0.97

**Final Recall:** 0.87

**Final F1-Score:** 0.92

**Key Conclusions**
*Ensemble Superiority:* Stacking and Voting methods consistently outperformed individual classifiers.

*High Precision Priority:* Maintaining a 97% Precision ensures that the system is safe for production, as the cost of a "False Positive" is extremely high in communication filters.

**Tech Stack**
*Language:* Python

*Libraries:* Scikit-learn, NLTK, Pandas, NumPy, Seaborn, Matplotlib
