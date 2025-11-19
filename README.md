# Sephora Customer Insight NLP Pipeline

**[📚 View "Group5 Slides" for detailed Info (PDF)]**
---

## Project Overview: Transforming Reviews into Strategic Intelligence
This project addresses the challenge faced by e-commerce platforms like Sephora in extracting actionable insights from massive volumes of unstructured customer reviews.We designed and implemented a scalable **3-stage NLP pipeline** to automatically convert thousands of reviews into structured topics, sentiment scores, and final **product-level strategic recommendations**.

### Core Objectives
1.  **Quantify Sentiment:** Assign precise sentiment scores to each review using advanced models.
2.  **Discover Topics:** Identify specific product attributes discussed by customers through topic modeling.
3.  **Generate Strategy:** Produce concise Pros & Cons summaries and locate the most strategically valuable product/topic combinations.

---

## System Architecture: The 3-Stage Insight Pipeline
<img width="1011" height="264" alt="image" src="https://github.com/user-attachments/assets/c6fb0a9e-4512-4f96-9a95-2dff51f8b97a" />

### Stage 1: Sentiment Analysis
* **Technology:** Used a fine-tuned **BERT Model** (Regression-based approach) to predict review star ratings.
* **Goal:** Obtain granular, continuous sentiment scores for precise analysis.

### Stage 2: Weighted Topic Modeling (Core Contribution)
* **Technology:** A hybrid method combining **SBERT embeddings + K-Means Clustering** for initial grouping, refined using **LDA** for topic clarity.
* **Innovation:** Calculated **Weighted Sentiment Scores** for each topic based on frequency and severity, ensuring business relevance.

### Stage 3: Summary Generation & Strategic Output
* **Technology:** Deployed a **Mistral 7B LLM** to generate clear, concise **Pros & Cons summaries** for each identified topic cluster.
* **Final Output:** Generates a **Strategic Opportunity Matrix** to pinpoint high-volume, low-sentiment areas for immediate action.

---
## My Core Contribution

My primary responsibility centered on the crucial **Topic Modeling and Clustering** phase, ensuring the business insights were precise and actionable.

* **Core Contribution:** Implemented and optimized the **SBERT + K-Means Clustering model** (`Sbert_Kmeans.ipynb`) to cluster reviews into distinct, actionable product features.
* **Data Preporcessing:** Cleaned the raw text data and performed normalization and filtering necessary for accurate SBERT embedding generation.
* **Logic Development:** Developed the logic for calculating and applying the **Weighted Sentiment Score** to accurately reflect problem severity.
* **Tool Proficiency:** Demonstrated expertise in the end-to-end NLP workflow involving SBERT, K-Means, and downstream integration with LDA and LLMs.

---

## Setup and Execution

### Data Source

Raw review data was sourced from a public **Kaggle** dataset. The raw data files are **not** included in this repository. Please follow the instructions below:

* *Download:* Obtain the CSV file from the original Kaggle competition link (https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews).
* *Placement:* Place the CSV file into a `./data` directory to run the notebooks.



