# Pratilipi Recommendation System  

## 📌 Project Overview  
This project focuses on building a recommendation system for Pratilipi, an online storytelling platform. The goal is to predict and recommend pratilipis (stories) to users based on their historical reading behavior.  

The project implements multiple recommendation models and evaluates their performance.  

## 📊 Datasets  
The recommendation system is built using two datasets:  

- **`user_interaction.csv`**: Contains user interactions with pratilipis, including:  
  - `user_id`: Unique identifier for the user.  
  - `pratilipi_id`: Unique identifier for the pratilipi.  
  - `read_percent`: Percentage of the pratilipi read by the user.  
  - `updated_at`: Timestamp of the interaction.  

- **`metadata.csv`**: Contains metadata about pratilipis, including:  
  - `author_id`: Unique identifier of the author.  
  - `pratilipi_id`: Unique identifier of the pratilipi.  
  - `category_name`: Category of the pratilipi.  
  - `reading_time`: Estimated reading time in seconds.  
  - `published_at`: Timestamp when the pratilipi was published.  

The datasets are too large to be uploaded to GitHub. You can download them from the links below:  
- https://www.kaggle.com/datasets/soham0017/pratilipi-soham 

## 🔍 Exploratory Data Analysis (EDA)  
- Analyzed user interactions and pratilipi metadata.  
- Identified outliers in `read_percentage` (values exceeding 100).  
- Explored the most popular categories and trends in user engagement.  
- Created visualizations to understand reading behavior.  

## 🏗️ Implemented Models  
### **1️⃣ Popularity-Based Model**  
- Recommends pratilipis based on overall popularity (most read).  
- Useful for new users but lacks personalization.  

### **2️⃣ Collaborative Filtering (SVD)**  
- Uses Singular Value Decomposition (SVD) to predict user preferences.  
- Struggles with data sparsity, leading to poor predictions.  

### **3️⃣ Content-Based Filtering**  
- Recommends pratilipis based on metadata (category, author, reading time).  
- Uses cosine similarity and KNN to find similar pratilipis.  
- Lacks personalized user preferences, reducing accuracy.  

### **4️⃣ Hybrid Model (SVD + XGBoost)**  
- Combines collaborative filtering (SVD) with XGBoost for ranking.  
- Attempts to refine recommendations but fails due to weak initial SVD predictions.  

## 📉 Results & Findings  
- All models generated pratilipi recommendations.  
- However, the recommended pratilipis did not align with what users actually read.  
- Data sparsity and lack of strong user interaction signals resulted in poor model performance.  
- Future improvements should focus on deep learning techniques, better feature engineering, and richer user interaction data.  

## 🚀 Installation & Setup  
### Prerequisites  
Ensure you have Python 3.12 installed. Install dependencies using:  
```bash
pip install -r requirements.txt
```

### Download Datasets  
The datasets are too large to be stored in this repository. Download them from the links below:  
- [User Interaction  and Metadata Dataset](<https://www.kaggle.com/datasets/soham0017/pratilipi-soham>)   

After downloading, place them inside the `data/` folder.  

### Running the Jupyter Notebooks  
1. **EDA**: Run `EDA.ipynb` to explore the dataset.  
2. **Model Training**: Run `Recommender.ipynb` to train and evaluate recommendation models.  

## 🛠️ Tech Stack  
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)  
- **Surprise** (Collaborative Filtering)  
- **XGBoost** (Ranking Model)  
- **Jupyter Notebook** (EDA & Model Development)  
