# Aspect-Based Sentiment Analysis Triplet Extraction Character of Presidential Candidates on YouTube Comments Using PyABSA ASTE
Indonesia is entering a crucial political period in 2024 with the upcoming General Election to determine its new president and vice president. In this democratic landscape, evaluating the character of prospective leaders is paramount, significantly influencing public support. Amidst technological advancements, social media, particularly YouTube, has emerged as a vital platform for understanding and analyzing public sentiment and perceptions towards the candidates.

## 💡 Goal
The primary goal of this project is to analyze public sentiment towards presidential candidates as expressed in YouTube comments. Through this analysis, we aim to:
* Gain deep insights into how the public evaluates candidate characters based on detected sentiments.
* Understand the significant role of social media in shaping public perception and influencing modern political processes.
* Apply a state-of-the-art model (EMC-GCN) on real-world Indonesian social media data.

## 📦 What I Did
This project encompassed the following key stages:

1.  **Data Collection & Preprocessing:**
    * **Collection:** YouTube comment data was systematically collected from 27 videos uploaded by official Indonesian news channels (e.g., KOMPASTV, CNN Indonesia) related to the presidential candidates.
    * **Raw Data Format:** The collected data was stored in a CSV file, including key columns such as 'publishedAt', 'authorDisplayName', and 'textDisplay'.
    * **Cleaning & Preparation:** The raw comment data underwent extensive cleaning and preprocessing to ensure data quality.
    * **Annotation Adjustment:** The annotation format was meticulously adjusted to conform to the specific input requirements of the EMC-GCN model, structured into aspect-opinion-sentiment triplets.

2.  **Model Implementation & Training:**
    * The official PyTorch implementation of the **EMC-GCN model** was utilized.
    * The model was trained on the prepared dataset using the following hyperparameters:
        * **Sequence Length:** 120
        * **Epochs:** 50
        * **Batch Size:** 8

3.  **Analysis & Visualization:**
    * Model outputs were thoroughly visualized and interpreted using various tools, including word clouds and detailed charts, to provide clear insights into sentiment distribution and aspect importance.
    * A comprehensive sentiment analysis was conducted based on the identified aspects and individual candidates.

## 🧰 Tools & Technologies
- Python, Pandas, PyABSA
- Matplotlib, WordCloud, Seaborn

## 📈 Results Summary
The analysis of public sentiment towards Indonesian presidential candidates revealed several significant findings:

* **Model Performance:**
    * The EMC-GCN model achieved a **maximum F1-score of 61.52%** during its training phase.
    * On the independent test dataset, the model demonstrated an **F1-score of 56.87%**.
    * While effective in predicting positive sentiment, the model frequently encountered challenges in accurately distinguishing neutral sentiment.

* **Dominant Sentiments and Key Aspects:**
    * Overall, the analysis indicated a **dominance of positive sentiment** across the comments.
    * This positive sentiment was particularly pronounced in aspects related to **'bicara' (talking/communication)** and **'debat' (debate performance)** for the candidates.

* **Candidate-Specific Sentiment Patterns:**
    * **Anies Baswedan:** Tended to receive negative sentiment primarily concerning the **'work' (kinerja)** aspect.
    * **Prabowo Subianto:** Showed negative sentiment more frequently related to his **'talking' (cara bicara)** and **'debate' (penampilan debat)** aspects.
    * **Muhaimin Iskandar:** Experienced negative sentiment in aspects concerning his **'answers' (jawaban)** and **'talking' (cara bicara)**.
    * **Ganjar Pranowo:** Exhibited a relatively balanced distribution of both positive and negative sentiment across various aspects.
    * **Gibran Rakabuming:** Received a predominantly **positive response** from the public comments analyzed.
    * **Mahfud MD:** Encountered negative sentiment in certain specific aspects of his character or performance.

This comprehensive analysis underscores the critical role of social media in shaping and reflecting public perceptions of potential leaders, offering valuable insights into candidate character evaluations based on detected sentiments within a dynamic political landscape.


## 📝 Credits
PyABSA original paper: https://arxiv.org/pdf/2208.01368 
Official code repo used: https://github.com/yangheng95/PyABSA
