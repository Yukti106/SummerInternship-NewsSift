A smart and flexible news recommendation engine that combines traditional Information Retrieval (IR) techniques with Machine Learning (ML) re-ranking models to deliver more relevant and ranked news articles for any user query.

🚀 Project Overview
This project first uses TF-IDF vectorization and cosine similarity to find news articles matching a user’s search query. Then, it improves these results using Learning-to-Rank models like Logistic Regression, Naive Bayes, and XGBoost Ranker to re-rank articles based on features like TF-IDF score, position, and headline length.

Performance is measured using Precision and NDCG scores to compare the effectiveness of each model.

A simple Streamlit web app allows anyone to enter a search query and instantly see the top recommended news headlines along with scores.

✨ Key Features
✅ Text Preprocessing: Cleans and lemmatizes news headlines and descriptions.
✅ TF-IDF & Cosine Similarity: Finds relevant documents based on query similarity.
✅ ML Re-Ranking: Re-ranks initial results using Logistic Regression, Naive Bayes, and XGBoost Ranker.
✅ Evaluation Metrics: Calculates Precision and NDCG to assess model performance.
✅ Interactive UI: Simple Streamlit app for user input and result display.
✅ Flexible Pipeline: Easy to extend with more features, better models, or real-time data.

📂 Project Structure
bash
Copy
Edit
📁 news-recommender/
 ├── ui.py              # Streamlit web app
 ├── news_main.py       # Main pipeline logic
 ├── project_plot.py    # Plots for evaluation
 ├── News_Category_Dataset_v3.json  # HuffPost news dataset
 ├── requirements.txt   # Python dependencies
 ├── README.md          # Project documentation
⚙️ How It Works
1️⃣ Load & Clean Data:
Loads news data from JSON, removes HTML tags, lowercases text, removes stopwords, and lemmatizes words.

2️⃣ IR Pipeline:
Uses TF-IDF Vectorizer to transform text and calculates cosine similarity between the query and all documents.

3️⃣ Initial Ranking:
Retrieves top matching articles based on similarity.

4️⃣ Feature Engineering:
Creates simple features like TF-IDF score, squared score, rank position, and headline length.

5️⃣ Machine Learning Re-Ranking:
Splits features into training/testing sets and trains Logistic Regression, Naive Bayes, and XGBoost models to re-rank.

6️⃣ Evaluation:
Measures Precision and NDCG scores for IR-only and ML re-ranking models.

7️⃣ Streamlit UI:
Takes user input query and displays the top-ranked headlines with scores.

📊 Example Output
markdown
Copy
Edit
Top matches re-ranked with XGBoost Ranker:
XGB Score: 1.2455
Headline: Learning To Be A College Mom
------------------------------------------------------------
XGB Score: 1.1890
Headline: This Magical Machine Claims To Keep Avocados Fresh
------------------------------------------------------------
🔬 Future Scope
✅ Add personalization using user history and clicks.
✅ Integrate real-time news feeds for live updates.
✅ Support multiple languages for diverse users.
✅ Use advanced models like BERT/Transformers for better text understanding.
✅ Improve UI with filters, bookmarks, and feedback loops.
✅ Build mobile or browser extensions for easy access.

📦 Tech Stack
Python 3.x

scikit-learn (Logistic Regression, Naive Bayes)

XGBoost

NLTK for text preprocessing

Streamlit for web interface

Pandas & NumPy for data handling

⚡ Getting Started
1️⃣ Clone the repo

bash
Copy
Edit
git clone https://github.com/yourusername/news-recommender.git
cd news-recommender
2️⃣ Install dependencies

bash
Copy
Edit
pip install -r requirements.txt
3️⃣ Run the Streamlit app

bash
Copy
Edit
streamlit run ui.py
4️⃣ Enter a query & see your top news recommendations!

🤝 Contributing
Pull requests, suggestions, and ideas for improvements are welcome! Feel free to fork and experiment.

📜 License
This project is for educational and research purposes.
Include your preferred license if needed.

✨ Contact
Created with ❤️ for learning IR, NLP, and ML ranking.
Feel free to reach out if you’d like to collaborate!


