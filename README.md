# 🎵 Music Recommendation System

## 🧠 Overview

This project builds a **personalized music recommendation system** using a rich dataset of 170,000+ tracks sourced from Spotify. By analyzing acoustic features such as **valence**, **energy**, **danceability**, and **tempo**, the system clusters similar songs and recommends tracks based on either **artist** or **genre** using machine learning techniques.

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `Music_Recommendation_Modeling.ipynb` | Jupyter notebook implementing preprocessing, clustering, and recommendation logic |
| `Music_Recommendation_Report.pdf` | Detailed report with methodology, evaluation, and analysis |
| `Music_Recommendation_System.pptx` | Slide deck summarizing the project |
| `data_by_artist.csv` | Aggregated features per artist |
| `data_by_genres.csv` | Genre-level song attributes |

---

## 📊 Dataset Description

- **Source:** [Kaggle Spotify Dataset](https://www.kaggle.com/datasets/vatsalmavani/spotify-dataset/data)
- **Time Range:** 1921–2020
- **Features:**  
  - Acousticness, Danceability, Energy, Tempo  
  - Popularity, Valence, Instrumentalness  
  - Artist metadata

---

## 🧪 Methodology

1. **Preprocessing & Normalization:**  
   - Standardized numerical features using `StandardScaler`  
   - Removed irrelevant features and missing values  

2. **Clustering:**  
   - Used **K-Means** and **Mini-Batch K-Means**  
   - Determined optimal clusters via **Elbow Method (k=4)**  
   - Evaluated with **Silhouette Score (~0.21)** and **Davies-Bouldin Score (~1.51)**

3. **Dimensionality Reduction:**  
   - **PCA** for visualizing cluster separation  
   - **t-SNE** for non-linear structure discovery  

4. **Recommendation Systems:**  
   - **Artist-Based:** Songs from the same cluster and artist  
   - **Genre-Based:** Songs from the same genre with similar acoustic profiles

---

## 📈 Key Results

| Algorithm            | Silhouette Score | Davies-Bouldin Score |
|----------------------|------------------|-----------------------|
| K-Means              | 0.21             | 1.5293                |
| Mini-Batch K-Means   | 0.21             | 1.5157                |

✅ **Mini-Batch K-Means** was more efficient and slightly more accurate on larger datasets.

---

## 💡 Sample Recommendations

- **Artist-Based Input:** "Diamonds" by Rihanna → recommends similar Rihanna tracks  
- **Genre-Based Input:** "Valentine's Day" → recommends genre-aligned songs like *Blinding Lights*

---

## 🚀 Future Work

- Integrate **DBSCAN** or **Hierarchical Clustering**  
- Add **collaborative filtering** for hybrid recommendations  
- Use **lyrics sentiment analysis** or **mood tagging** for deeper personalization  
- Explore **deep learning models** (e.g., autoencoders) for feature learning

---

## 🛠 Tools Used

- Python (Pandas, Scikit-learn, NumPy, Matplotlib)  
- Jupyter Notebook  
- PCA and t-SNE for visualization  
- K-Means and Mini-Batch K-Means clustering

---
