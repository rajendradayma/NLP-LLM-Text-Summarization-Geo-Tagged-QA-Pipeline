# NLP-LLM-Text-Summarization-Geo-Tagged-QA-Pipeline
Objective

Build a system that can:
- Summarize long-form news articles (from CNN-DailyMail).
- Extract geographic locations from text and geocode them.
- (Optional) Answer questions from the article using LLM or open-source frameworks.
- Save output as a CSV file containing:
  - Summarized article
  - Geolocations (lat, lon)
  - (Optional) QA response

---

## 📂 Dataset

**CNN-DailyMail News Text Summarization**  
[Kaggle Dataset Link](https://www.kaggle.com/datasets/gowrishankarp/newspaper-text-summarization-cnn-dailymail)

Files:
- `train.csv`
- `test.csv`
- `validation.csv`

Each row contains:
- `article`: The full news article
- `highlights`: Ground-truth human-written summary (for validation)

---

## 🛠️ Tech Stack

- **Transformers**: `facebook/bart-large-cnn` or `t5-base` for summarization
- **SpaCy**: Named Entity Recognition (NER) to extract GPE (geo-political entities)
- **Geopy**: Convert extracted places into latitude/longitude
- **Pandas**: Data loading and saving
- **Google Colab**: For GPU-powered execution

---

## 📦 Installation

```bash
pip install transformers
pip install torch
pip install spacy
pip install geopy
python -m spacy download en_core_web_sm
