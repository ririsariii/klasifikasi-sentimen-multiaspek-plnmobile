# 📊 Aspect-Based Sentiment Analysis on PLN Mobile App Reviews

This repository contains the implementation of my undergraduate thesis project entitled:

**"Aspect-Based Sentiment Analysis on PLN Mobile Application Reviews Using Topic Modeling and Machine Learning Approaches"**

The project aims to analyze user reviews from the PLN Mobile application by identifying discussed aspects and classifying sentiments into positive, neutral, or negative categories.

The research combines:
- Data Scraping
- Natural Language Processing (NLP)
- Topic Modeling (LDA)
- Sentiment Classification
- Data Balancing Techniques
- Performance Evaluation

---

# 🎯 Research Objectives

- Identify important aspects discussed by PLN Mobile users.
- Analyze public sentiment toward PLN Mobile services.
- Compare classification performance:
  - Without SMOTE-Tomek
  - With SMOTE-Tomek
- Evaluate model performance using AUC metrics.

---

# 🛠️ Technologies & Libraries

## Programming Language
- Python

## Libraries & Tools
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Sastrawi
- Gensim
- Matplotlib
- Seaborn
- imbalanced-learn
- pyLDAvis
- Google Play Scraper
- App Store Scraper

## Development Tools
- Jupyter Notebook
- Google Colab
- VS Code

---

# 📂 Research Workflow

---

# 1️⃣ Scraping Google Play Store

This stage collects PLN Mobile application reviews from the Google Play Store using scraping libraries.

### Activities:
- Retrieve user reviews
- Retrieve ratings
- Retrieve review dates
- Store reviews into CSV format

### Output:
```bash
googleplay_reviews.csv
```

---

# 2️⃣ Scraping Apple App Store

Collect user reviews from Apple App Store to enrich dataset diversity.

### Activities:
- Scrape iOS PLN Mobile reviews
- Merge metadata
- Save results into CSV

### Output:
```bash
appstore_reviews.csv
```

---

# 3️⃣ File Merging

Combine review datasets from:
- Google Play Store
- Apple App Store

### Activities:
- Merge CSV files
- Standardize column names
- Remove duplicate structures

### Output:
```bash
merged_dataset.csv
```

---

# 4️⃣ Dataset Recovery

Recover incomplete or corrupted dataset rows before preprocessing.

### Activities:
- Handle broken records
- Recheck missing fields
- Validate review entries

### Output:
```bash
recovered_dataset.csv
```

---

# 5️⃣ Exploratory Data Analysis (EDA)

Analyze dataset characteristics before preprocessing.

### Activities:
- Review distribution visualization
- Rating distribution analysis
- Word frequency analysis
- Data imbalance observation

### Visualization:
- Bar chart
- Pie chart
- Word cloud

---

# 6️⃣ Data Cleaning

Clean noisy and irrelevant data.

### Activities:
- Remove duplicates
- Remove URLs
- Remove emojis
- Remove punctuation
- Remove numbers
- Remove special characters

### Output:
```bash
cleaned_dataset.csv
```

---

# 7️⃣ Text Preprocessing

Prepare text data for NLP processing.

### Activities:
- Case folding
- Tokenization
- Stopword removal
- Stemming using Sastrawi
- Normalization

### Output:
```bash
preprocessed_dataset.csv
```

---

# 8️⃣ Removing Missing Values After Preprocessing

Remove empty rows generated after preprocessing.

### Activities:
- Detect null values
- Remove blank reviews
- Validate dataset consistency

### Output:
```bash
final_preprocessed_dataset.csv
```

---

# 9️⃣ Topic Modeling

Apply Latent Dirichlet Allocation (LDA) to identify aspects discussed in PLN Mobile reviews.

### Activities:
- Create document-term matrix
- Train LDA model
- Extract dominant topics
- Label generated aspects

### Example Topics:
- Login issues
- Payment services
- Application performance
- Electricity token purchase
- Customer service

---

# 🔟 LDA Topic Visualization

Visualize topic modeling results using interactive visualization.

### Activities:
- Generate pyLDAvis visualization
- Observe topic relevance
- Analyze intertopic distance

### Tools:
- pyLDAvis
- Matplotlib

---

# 1️⃣1️⃣ Krippendorff Alpha

Evaluate annotation reliability for sentiment labeling.

### Activities:
- Inter-rater agreement calculation
- Label consistency validation

### Purpose:
Ensure sentiment labels are reliable before classification.

---

# 1️⃣2️⃣ Classification Without SMOTE-Tomek

Perform sentiment classification using original imbalanced dataset.

### Activities:
- Train machine learning model
- Evaluate classification performance
- Generate confusion matrix

### Metrics:
- Accuracy
- Precision
- Recall
- F1-Score

---

# 1️⃣3️⃣ Classification With SMOTE-Tomek

Handle class imbalance using SMOTE-Tomek technique before classification.

### Activities:
- Oversampling minority class
- Tomek Links cleaning
- Retrain classification model

### Goal:
Improve minority class prediction performance.

---

# 1️⃣4️⃣ AUC Calculation

Evaluate model performance using Area Under Curve (AUC).

### Activities:
- Generate ROC Curve
- Calculate AUC score
- Compare model performance

### Evaluation:
- Without SMOTE-Tomek
- With SMOTE-Tomek

---

# 📊 Research Results

The implementation successfully:
- Extracted aspects from PLN Mobile reviews
- Classified sentiments into multiple categories
- Improved classification performance using SMOTE-Tomek
- Visualized topic modeling results effectively

---

# 🚀 How to Run the Project

## 1. Clone Repository

```bash
git clone https://github.com/ririsariii/klasifikasi-sentimen-multiaspek-plnmobile.git
```

---

## 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 3. Open Jupyter Notebook

```bash
jupyter notebook
```

---

## 4. Run Notebook Sequentially

Execute notebooks step-by-step according to research stages.

---

# 👩‍💻 Researcher

**Yuliani Purwitasari**  
Information Systems UPN Veteran Jawa Timur

GitHub:  
https://github.com/ririsariii

---

# 📄 License

This project is developed for educational, research, and portfolio purposes.
