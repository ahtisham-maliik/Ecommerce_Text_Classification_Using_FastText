# Ecommerce Text Classification Using FastText

![Ecommerce Text Classification Using FastText](cover__photo.png)

## Overview
This project implements a text classification system for e-commerce product descriptions using FastText. The model categorizes products into 4 distinct categories with 95.57% accuracy, demonstrating FastText's effectiveness for text classification tasks with minimal preprocessing.

## Dataset
- **Source**: `ecommerce_dataset.csv`
- **Initial Size**: 50,425 entries
- **Final Size**: 27,802 entries after cleaning
- **Features**:
  - `category`: Product category (4 classes)
  - `description`: Product description text

### Category Distribution
| Category                | Count  | Percentage |
|-------------------------|--------|------------|
| Household               | 10,564 | 38.0%      |
| Books                   | 6,256  | 22.5%      |
| Clothing & Accessories  | 5,674  | 20.4%      |
| Electronics             | 5,308  | 19.1%      |

## Data Preprocessing
### Cleaning Steps:
1. Removed 1 entry with missing description
2. Eliminated 22,622 duplicate entries
3. Normalized category names (e.g., "Clothing & Accessories" → "Clothing_and_Accessories")

### Text Processing Techniques
- **Lemmatization**: Reduced words to their base/dictionary form (e.g., "paintings" → "painting")
- **Lowercasing**: Converted all text to lowercase for consistency
- **Stopword removal**: Eliminated common words (e.g., "the", "is", "and")
- **Punctuation removal**: Removed special characters (e.g., commas, periods, quotes)

**Result**: Reduced average description length by ~30% (346 → 243 characters)

## 🧪 Model Training

### 📂 Dataset Split

| Dataset | Size   | Percentage |
|---------|--------|------------|
| Train   | 22,241 | 80%        |
| Test    | 5,561  | 20%        |

---

## 📈 Evaluation Results

### 🧪 Test Performance

- **Precision**: `95.57%`  
- **Recall**: `95.57%`  
- **Test Samples**: `5,561`  

---

## 📦 Dependencies

To replicate this project, make sure the following packages are installed:

- Python 3.10  
- `pandas`  
- `scikit-learn`  
- `fasttext`  
- `spaCy` with the `en_core_web_sm` model  

---

## 🔍 Key Insights

- Achieved **95.57% accuracy** with **minimal preprocessing**
- **Text normalization** significantly improves model performance:
  - Lemmatization reduces vocabulary size
  - Stopword removal focuses on meaningful terms
- **FastText Advantages**:
  - Handles short product descriptions effectively
  - Requires minimal computational resources
  - Captures semantic relationships through subword information
- **Category prefix formatting** (`__label__`) is essential for FastText
- **Embedding-based approach** enables semantic similarity searches
- The solution demonstrates **FastText's effectiveness** for e-commerce classification, providing **high accuracy** with **efficient training** suitable for production environments.
