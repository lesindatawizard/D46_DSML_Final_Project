# D46_DSML_Final_Project

# 🎬 Final Capstone Project – EntriElevate  
## Movie Recommendation Engine Using Content-Based Filtering

This capstone project focuses on building a **Content-Based Movie Recommendation System** using a real-world movie dataset. The system uses movie metadata such as **plot summaries, genres, and cast** to recommend similar movies. Unlike supervised ML techniques, this project leverages **unsupervised learning** through similarity computation—providing an alternative use of machine learning in recommender systems.

## 📁 Dataset Source  
- **Dataset**: Rotten Tomatoes Movies Metadata  
- **Approximate Size**: ~16,000+ records  
- **Features Used**: `movie_title`, `movie_info` (plot), `genre`, `cast`  
- **Note**: The dataset contains missing values and inconsistent entries, which were handled during preprocessing.

## ✅ Steps Done in the Project

### 1. Dataset Cleaning
- Removed duplicate rows
- Capped long plot summaries (outlier treatment using IQR)
- Replaced missing values with `'N.A'` in categorical features
- Extracted and retained key columns: `movie_info`, `genre`, `cast`, `rating`, and `movie_title`

### 2. Exploratory Data Analysis (EDA)
- Bar charts and pie plots to identify genre popularity
- Frequency analysis of top directors and cast members
- Rating distribution and plot length boxplots
- Visual insights on missing data and content spread

### 3. Feature Engineering & Encoding
- Plot summaries vectorized using **TF-IDF**
- Genres and cast were encoded using multi-hot representation
- Combined features into a single content profile for each movie

### 4. Similarity Computation
- Used **Cosine Similarity** to compute similarity scores between movie vectors
- Created a similarity matrix for content comparison

### 5. Recommendation System
- Developed a function `recommend_movies()` to return top-N similar movies
- Handled fuzzy matching for incorrect movie titles
- Added interactive input loop for continuous movie search
- Displayed genre along with recommended movie names

## 📈 Key Outcomes
- Successfully built a content-based recommender system using NLP and vector similarity
- Incorporated outlier treatment, missing data handling, and feature merging
- Enhanced usability with fuzzy search correction and genre display
- Interactive CLI interface for user-friendly recommendations

## 🛠️ Tools & Technologies Used
- Python, Pandas, NumPy  
- Scikit-learn (TF-IDF, cosine similarity)  
- Seaborn, Matplotlib (visualizations)  
- FuzzyWuzzy (fuzzy matching)

## 🔍 Conclusion & Insights
- Content-based filtering works effectively without relying on user data
- Plot summaries and genre together offer strong indicators for similarity
- Data quality (missing values, plot length) significantly impacts recommendations
- Project showcases practical use of **unsupervised learning** in ML pipelines

## 🚀 Future Enhancements
- Integrate BERT or transformer-based models for deeper plot understanding  
- Add collaborative filtering for hybrid recommendations  
- Deploy a Streamlit app for a GUI experience  
- Add filtering by release year or rating
