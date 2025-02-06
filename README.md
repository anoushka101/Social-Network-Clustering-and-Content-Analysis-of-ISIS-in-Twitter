
## Social Network Cluster and Content Analysis of ISIS in Twitter  

### 📖 Overview  

This project analyzes the pro-ISIS Twitter network by identifying influential accounts and analyzing the content of their tweets. Using a dataset of over 17,000 tweets collected from more than 100 pro-ISIS Twitter accounts, this study applies **social network analysis (SNA)** and **machine learning** techniques to understand how ISIS propaganda spreads on Twitter.  

### 🔍 Research Questions  

- **Who are the top influencers in the pro-ISIS Twitter network?**  
- **What topics are pro-ISIS users discussing?**  

### 📂 Data  

- **Source:** [Kaggle Dataset](https://www.kaggle.com/datasets/fifthtribe/how-isis-uses-twitter/data)  
- **Size:** 4.5MB (17,410 rows, 8 columns)  
- **Columns:** Name, username, description, location, follower count, status count, timestamp, tweet text  

### 📊 Methodology  

#### 1️⃣ **Data Preprocessing**  
- Removed missing values, duplicates, URLs, mentions, hashtags, special characters, numbers, and stop words.  
- Standardized timestamps and performed **lemmatization** for text normalization.  

#### 2️⃣ **Sentiment & Thematic Analysis**  
- Used **Empath Library** to classify tweets into five categories:  
  - **Propaganda** (promoting violence/extremism)  
  - **Weapons**  
  - **Terrorism**  
  - **Crime**  
  - **Religion**  
- Applied **TF-IDF embeddings** and **Logistic Regression** to predict categories.  
- Evaluated the model with accuracy, precision, recall, and F1-score.  

#### 3️⃣ **Social Network Analysis (SNA)**  
- Constructed a **directed graph** where nodes represent Twitter users and edges represent mentions.  
- Computed **in-degree (mentions received)** and **out-degree (mentions made)**.  
- Applied **Louvain algorithm** for community detection.  
- Used **closeness centrality** and **degree-based ranking** to identify key influencers.  

### 📈 Results  

#### Sentiment & Thematic Analysis  
| Category      | Tweet Count | F1-Score (%) |
|--------------|------------|-------------|
| **Propaganda**  | 12,208      | 92%         |
| **Weapons**     | 2,178       | 85%         |
| **Terrorism**   | 856         | 73%         |
| **Crime**       | 792         | 68%         |
| **Religion**    | 419         | 49%         |

#### Social Network Analysis  
- **Top influencers**: Rami AlLolah, Nidalgazaui  
- Influencers were ranked based on **centrality measures** and **in-degree ranking**.  
- **Community detection** revealed tightly knit extremist subgroups.  

### 🚧 Limitations  
- The dataset only represents a **partial** Twitter network, limiting generalizability.  
- Some **categories had lower classification performance** due to imbalance in data.  
- Additional network data could **improve analysis and reduce bias**.  

### 📚 References  
1. **Benigni, Joseph & Carley (2017):** [Detecting ISIS Communities on Twitter](https://doi.org/10.1371/journal.pone.0181405)  
2. **Ali (2016):** [Social Network Analysis for Identifying Terrorist Affiliations](https://scholar.valpo.edu/ms_ittheses/1)  
3. **Peele (2015):** [ISIS Propaganda and Twitter Networks](https://doi.org/10.17615/dnph-vm42)  

### 🛠️ Technologies Used  
- **Python**: Pandas, NLTK, Scikit-learn  
- **Empath Library** for linguistic analysis  
- **Gephi** for social network visualization  
- **Logistic Regression** for sentiment classification  


