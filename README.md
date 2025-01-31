# 🎤 TED Talk Text: Word Frequency for Index Compression  

## 📜 Overview  
This project analyzes the **'description' column** from the **TED Talks dataset ("ted_main.csv")**, which contains metadata for all TED Talks uploaded until **September 21st, 2017**. Using **NLTK**, we preprocess text in multiple schemes to extract **word token statistics** and analyze vocabulary trends.  

📌 **Goals**:  
- Perform **three text processing schemes**:  
  - **[A] Word Tokenization Only**  
  - **[B] Tokenization + Case Folding + Stopword Filtering + Non-Alphabet Filtering**  
  - **[C] Scheme B + Porter Stemming**  
- Compute **word statistics** for each scheme:
  1. **Total Number of Tokens**  
  2. **Vocabulary Size**  
  3. **Top 30 Most Frequent Tokens**  
  4. **Coverage of Top 30 Tokens in Dataset**  
- Summarize results and **analyze vocabulary reduction trends**.

## 📊 Text Processing Steps  
### **1️⃣ Data Loading & Preprocessing**
- Load **"ted_main.csv"** (`utf-8` encoding).  
- Extract the **'description' column** (removing empty values).  
- Apply **three text processing schemes** to analyze vocabulary.
### **2️⃣ Text Processing Schemes**  
#### **[A] Word Tokenization Only**  
- Tokenize descriptions using `nltk.word_tokenize()`.  
- Compute total **tokens, vocabulary size, and frequency distribution**.  
#### **[B] Case Folding + Stopword Removal + Non-Alphabet Filtering**  
- Convert text to **lowercase**.  
- Remove **stopwords** (`NLTK stopword list`).  
- Remove **non-alphabetic tokens** (`isalpha()` function).  
- Compute total **tokens, vocabulary size, and frequency distribution**.  
#### **[C] Porter Stemming (On Top of Scheme B)**  
- Apply **Porter Stemming** (`nltk.PorterStemmer()`).  
- Compute total **tokens, vocabulary size, and frequency distribution**.

## 📊 Summary Table
![Summary Table](https://github.com/pngo1997/Images/blob/main/Inverted%20Index.png)  

## 🚀 Technologies Used  
🛠 **Libraries & Tools**:  
- **Python 3**  
- **NLTK (Natural Language Toolkit)**  
- **Pandas (for CSV processing)**  
- **Jupyter Notebook (`.ipynb`)**  

📡 **Dataset Source**: [TED Talks Metadata](https://www.ted.com/)  
