# 🐉 Game of Thrones NLP (Word2Vec Model)

This project builds a **Word2Vec model** using text data from the **Game of Thrones books**.  
It learns relationships between words and helps find similar characters, word meanings, and vector representations.

---

## 📌 What this project does

- Loads GOT book text files
- Cleans and preprocesses text
- Tokenizes sentences into words
- Trains a **Word2Vec model (Gensim)**
- Finds similar words (e.g., characters)
- Performs word similarity comparisons
- Detects odd words using "doesn't match"
- Converts words into vectors
- Applies **PCA for dimensionality reduction**
- Visualizes word vectors in 3D

---

## 🛠️ Tech Stack

- Python
- NLTK (for preprocessing)
- Gensim (Word2Vec model)
- Scikit-learn (PCA)
- Plotly (3D visualization)
- NumPy, Pandas

---

## 📂 Project Workflow

### 1. Data Loading
- Reads multiple GOT book text files from a folder

### 2. Text Preprocessing
- Sentence tokenization using NLTK
- Lowercasing text
- Removing stopwords
- Word tokenization using `simple_preprocess`

### 3. Model Training
- Word2Vec model trained with:
  - `window = 8`
  - `min_count = 10`
  - `epochs = 5`

### 4. Model Usage

#### 🔹 Similar Words
```python
model.wv.most_similar("jon")
