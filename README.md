# 🎬 Movie Recommender System

A content-based movie recommendation system leveraging machine learning to provide personalized movie suggestions based on genre and metadata features.

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Python](https://img.shields.io/badge/Python-3.8+-green.svg)
![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Algorithm](#algorithm)
- [Results](#results)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## 🎯 Overview

This project implements a **content-based filtering** recommendation system that analyzes movie metadata and genres to suggest similar movies to users. The system uses **cosine similarity** to find movies with comparable characteristics, enabling personalized recommendations without requiring user ratings or collaborative data.

## ✨ Features

- **Content-Based Filtering**: Recommends movies based on genre and metadata features
- **Cosine Similarity Analysis**: Utilizes TF-IDF and cosine similarity metrics for accurate recommendations
- **Easy-to-Use Interface**: Simple function calls to get recommendations
- **Dataset Integration**: Uses the comprehensive TMDB Movie Metadata dataset
- **Exploratory Data Analysis**: Includes detailed EDA and visualization notebooks

## 📊 Dataset

This project uses the **TMDB Movie Metadata** dataset from Kaggle.

- **Source**: [TMDB Movie Metadata - Kaggle](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
- **Size**: Comprehensive collection of movie data
- **Features Used**: 
  - Genres
  - Cast information
  - Crew details
  - Keywords
  - Plot summaries

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook
- pip or conda

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/Nayon09/Movie-Recommender-System.git
   cd Movie-Recommender-System
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the dataset**
   - Visit [Kaggle TMDB Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
   - Download and place the CSV files in the `data/` directory

## 📖 Usage

### Running the Notebook

1. Start Jupyter Notebook
   ```bash
   jupyter notebook
   ```

2. Open the main analysis notebook and follow the cells sequentially

### Getting Recommendations

```python
# Load the recommendation model
recommendations = recommend_movies(movie_title="The Matrix", num_recommendations=5)
print(recommendations)
```

## 🔧 Algorithm

### Methodology

1. **Data Preprocessing**
   - Handle missing values
   - Extract and clean genre information
   - Normalize metadata features

2. **Feature Engineering**
   - Create TF-IDF vectors from genre and keyword data
   - Combine multiple features into a unified feature matrix

3. **Similarity Calculation**
   - Apply cosine similarity to compute similarity scores between movies
   - Rank movies by similarity to the input movie

4. **Recommendation Generation**
   - Return top-N most similar movies
   - Present recommendations with relevance scores

### Key Metrics

- **Cosine Similarity Score**: Range [0, 1] - Higher values indicate greater similarity
- **Similarity Matrix**: Pairwise comparison of all movies

## 📈 Results

The system successfully identifies and recommends movies with similar:
- Genres
- Plot themes
- Cast and crew
- Keywords and themes

### Performance Characteristics

- Fast computation for recommendation generation
- Accurate similarity matching based on content features
- Scalable to large movie datasets

## 📁 Project Structure

```
Movie-Recommender-System/
├── README.md                 # Project documentation
├── LICENSE                   # MIT License
├── CONTRIBUTING.md          # Contribution guidelines
├── requirements.txt         # Python dependencies
├── .gitignore              # Git ignore rules
│
├── data/
│   ├── movies_metadata.csv # TMDB dataset
│   └── README.md           # Data documentation
│
├── notebooks/
│   ├── 01_EDA.ipynb        # Exploratory Data Analysis
│   ├── 02_Data_Preprocessing.ipynb
│   ├── 03_Model_Building.ipynb
│   └── 04_Recommendations.ipynb
│
├── src/
│   ├── __init__.py
│   ├── preprocessing.py    # Data preprocessing functions
│   ├── similarity.py       # Similarity calculation functions
│   └── recommender.py      # Recommendation engine
│
└── output/
    └── results.csv         # Recommendation results
```

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to contribute to this project.

### Steps to Contribute

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Nayon09**
- GitHub: [@Nayon09](https://github.com/Nayon09)
- Repository: [Movie-Recommender-System](https://github.com/Nayon09/Movie-Recommender-System)

---

## 📞 Support & Feedback

- 📧 Open an issue for bug reports or feature requests
- 💬 Discussions are welcome in the GitHub Discussions section
- ⭐ If you find this helpful, please consider starring the repository!

## 🔮 Future Enhancements

- [ ] Collaborative filtering implementation
- [ ] Hybrid recommendation system
- [ ] User interface/web application
- [ ] Real-time recommendation API
- [ ] Advanced NLP for better feature extraction
- [ ] Deep learning models (Neural Networks, Autoencoders)

---

**Last Updated**: May 10, 2026
