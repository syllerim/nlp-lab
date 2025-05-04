![Keepcoding](keepcoding.png)

# 💬 NLP – Sentiment Analysis Assignment 🧐

✍️ **Author:** Mirellys Arteta Davila

This project is part of the **Natural Language Processing** (NLP) module from the **KeepCoding AI Bootcamp**.  
The objective is to build and evaluate a **sentiment analysis** pipeline using **Amazon product reviews**.

---

## 📁 Structure

- **EDA** → download + data exploration. 
- **Preprocessing** → Text cleaning pipeline.
- **Modeling** → Training & comparing 2 Machine Learning and 1 Deep Learning sentiment classifiers.
- **Reports** → Metrics, evaluation and conclusions.

---

## 📦 Dataset

- Small subsets for experimentation [Amazon Reviews](https://jmcauley.ucsd.edu/data/amazon/) → [Data 2018 5-core](https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/)
	
	- [Amazon Fashion - 3176 reviews](https://mcauleylab.ucsd.edu/public_datasets/data/amazon_v2/categoryFilesSmall/AMAZON_FASHION_5.json.gz)
	
	- [Appliances - 2277 reviews](https://mcauleylab.ucsd.edu/public_datasets/data/amazon_v2/categoryFilesSmall/Appliances_5.json.gz)
	
	- [Software - 12805 reviews](https://mcauleylab.ucsd.edu/public_datasets/data/amazon_v2/categoryFilesSmall/Software_5.json.gz)
	
- Format: one-review-per-line in JSON. 

**Sample Review:**

```
{
"image": ["https://images-na.ssl-images-amazon.com/images/I/71eG75FTJJL._SY88.jpg"], 
"overall": 5.0, 			   // rating of the product
"vote": "2",                   // helpful votes of the review
"verified": True, 
"reviewTime": "01 1, 2018",    // time of the review (raw)
"reviewerID": "AUI6WTTT0QZYS", // ID of the reviewer
"asin": "5120053084",          // ID of the product
"style": {                     // Dictionary of the product metadata
	"Size:": "Large", 
	"Color:": "Charcoal"
	},                          
"reviewerName": "Abbey",       // Name of the reviewer 
"reviewText": "I now have 4 of the 5 available colors of this shirt... ", 
"summary": "Comfy, flattering, discreet--highly recommended!", 
"unixReviewTime": 1514764800   // time of the review (unix time)
}
```

- Preprocessing: only reviews with ratings (1–5)
- Sentiment labels created from star ratings:

| Stars         | Sentiment Label | Category     |
|---------------|------------------|--------------|
| ⭐️           | 0                | Negative     |
| ⭐️⭐️         | 0                | Negative     |
| ⭐️⭐️⭐️       | removed          | Neutral     |
| ⭐️⭐️⭐️⭐️     | 1                | Positive     |
| ⭐️⭐️⭐️⭐️⭐️   | 1                | Positive     |


---

## 🛠️ Tools & Libraries

- Python
- pandas, matplotlib, numpy, seaborn
- nltk, wordcloud, scikit-learn
