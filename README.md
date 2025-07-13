# 💬 WhatsApp Chat Analysis – Flirt Prediction & Sentiment Insight

This project performs smart analysis on a WhatsApp chat between two people — identifying **flirtatious messages**, analyzing **sentiment**, and extracting **behavioral patterns** like talkativeness, media sharing, and missed calls.

---

## 📌 Objectives

- 🧠 Predict whether a message is **flirtatious** (label 1) or **not** (label 0)
- 😊 Perform **sentiment analysis** on each message
- 📊 Analyze user behavior: most active hours, media count, talkativeness
- 📅 Find **most active day/time**
- 📞 Identify missed calls

---

## 🧰 Tech Stack

- Python 🐍
- pandas, matplotlib, seaborn
- sklearn (for flirt prediction)
- textblob or nltk (for sentiment analysis)

---

## 📂 Dataset Format (Preprocessed)

| Date      | Time    | Name     | Chat                                       | Flirt |
|-----------|---------|----------|--------------------------------------------|--------|
| 12/07/25  | 10:01pm | Alex 💬   | You always have the best playlists… 😅     | 1      |
| 12/07/25  | 09:15am | Jamie 🎧  | Don’t forget your notebook!               | 0      |

---

## 🧪 Model - Flirt Detection

- Features: Message text (`Chat`)
- Labels: `Flirt` column (manually tagged as 0 or 1)
- Vectorization: CountVectorizer / TF-IDF
- Classifier: Logistic Regression

```python
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
