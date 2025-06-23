# Data Collection for Classifying Palestinian News (Real/Fake) - web scraping


---

## 1. Introduction  
The goal of this task was to prepare a dataset for classifying Palestinian news articles as **Real** or **Fake** using NLP techniques. We focused on news that is clearly related to Palestine, collected from a variety of sources to ensure balance.

---

## 2. Data Collection  
- Collected **403 news articles** about Palestine.  
- Most articles were from **January 2024**; a few dated before October 2023.  
- **Real news (300)** came from trusted sources like **Al Jazeera**, **Misbar**, and official Palestinian websites.  
- **Fake news (103)** came from social media platforms (Twitter, Facebook, YouTube) and suspicious sites.

---

## 3. Data Extraction  
- Used **web scraping** (`newspaper3k`) to extract titles and content.  
- Manually copied news from official Palestinian websites.  
- Extracted **publish dates** using `urllib.parse`.

---

## 4. Data Cleaning  
- Removed **URLs, ads, random symbols**, and unrelated articles.  
- Kept only news **clearly focused on Palestine**.

---

## 5. Data Organization  
- Combined all entries into one dataset.  
- Added an **ID column** for unique identification.  
- Labeled sources:  
  - Trusted media (e.g., Al Jazeera, official websites) → **Real**  
  - Social media or flagged content → **Fake**, based on Misbar, Tayqan, Tahaqaq, Chayyek.

---

## 6. Saving the Dataset  
- Saved as `GroupC_NLP_Task3.csv`.  
- Dataset contains **403 rows**:  
  - **300 Real**, **103 Fake**  
  - Columns: `ID`, `title`, `content`, `date`, `label`

---

*This dataset is now ready for use in classification models for detecting misinformation in Palestinian news.*
