# Movie Recommendation System Using Deep Learning

**Personalised Movie Recommendations | Neural Networks | Predictive Modelling**

An end-to-end machine learning project exploring how neural networks can predict user preferences and support personalised movie recommendations.

The system uses a Multi-Layer Perceptron (MLP) with user and movie embeddings to learn relationships between users, movies and historical ratings. It uses collaborative filtering through learned user and movie embeddings to estimate ratings and generate recommendations. Movie metadata is used only for optional title lookup through the correct MovieLens-to-TMDb mapping.

## Project Overview

Recommendation systems help users discover relevant content by analysing historical interactions and identifying patterns in preferences.

This project investigates how deep learning can be applied to movie recommendation by combining user–movie interaction data with additional movie information.

**Project objectives:**
- Explore and preprocess movie ratings and metadata.
- Identify patterns in user preferences and movie characteristics.
- Develop a neural network-based rating prediction model.
- Evaluate predictive performance using regression metrics.
- Explore personalised recommendations using predicted ratings and genre preferences.

## Technology Stack

| Category | Technologies |
|---|---|
| Programming | Python |
| Deep Learning | TensorFlow, Keras |
| Data Analysis | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Visualisation | Matplotlib, Seaborn |
| Development | Jupyter Notebook |

## Dataset

The project uses data from [The Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset), including:

- **ratings_small.csv:** Historical user ratings for movies.
- **movies_metadata.csv (optional):** Movie titles and metadata for display.
- **links_small.csv (optional):** Maps MovieLens movie IDs to TMDb movie IDs; required when using movie metadata.

The data supports the analysis of user–movie interactions and the preparation of features for neural network training.

Dataset files are not included in this repository. They can be downloaded from the original source.

## Methodology

### 1. Data Preparation

The workflow begins with exploring the datasets, handling missing values, preparing relevant features and transforming categorical and numerical information into a suitable format for model training.

### 2. Feature Engineering

User and movie identifiers are represented through learned embeddings, allowing the model to capture patterns in historical rating behaviour.

Movie metadata is not used as a model feature in the corrected notebook. Optional title lookup uses `links_small.csv` to avoid mismatched movie IDs.

### 3. Neural Network Development

A Multi-Layer Perceptron is implemented using TensorFlow/Keras to estimate movie ratings.

The model learns from user–movie interactions and associated features to produce predicted ratings.

### 4. Model Evaluation

Predictive performance is assessed using:

- **Mean Absolute Error (MAE):** Measures the average absolute difference between predicted and actual ratings.
- **Mean Squared Error (MSE):** Measures the average squared prediction error, placing greater emphasis on larger errors.

### 5. Recommendation Generation

The notebook explores a recommendation function that combines predicted ratings with genre preferences to identify potentially relevant movies for a user.

## Model Performance

The **archived original academic notebook** recorded the following results. These are **not metrics for the corrected notebook**, which must be rerun:

| Evaluation Metric | Recorded Result |
|---|---|
| Test Mean Absolute Error | **0.7344** |
| Test Mean Squared Error | **0.8811** |

The corrected notebook calculates fresh metrics when run and compares the MLP with a mean-rating baseline. No new accuracy result is claimed until that run is completed.

## Key Skills Demonstrated

- Exploratory data analysis and data preprocessing
- Feature engineering and categorical encoding
- Neural network architecture and embedding layers
- Deep learning model training using TensorFlow/Keras
- Regression-based model evaluation
- Recommendation system development
- Translating machine learning concepts into a practical application

## Repository Structure

```text
movie-recommendation-system/
├── movie_recommendation.ipynb
├── README.md
├── requirements.txt
├── .gitignore
├── DATA_VALIDATION.md
├── archive/
│   └── movie_recommendation_original.ipynb
└── data/
    └── .gitkeep
```

## Getting Started

**1. Clone the repository**

```bash
git clone https://github.com/vasudha99/movie-recommendation-system.git
cd movie-recommendation-system
```

**2. Install the required libraries**

```bash
python -m pip install -r requirements.txt
```

**3. Download the datasets**

Download `ratings_small.csv` from the dataset source and place it in `data/`. To display movie titles, also download `links_small.csv` and `movies_metadata.csv` into the same folder.

**4. Run the notebook**

Open `movie_recommendation.ipynb` using Jupyter Notebook or VS Code and execute the cells sequentially.

## Future Improvements

Potential extensions include:

- Strengthening the train/test preprocessing pipeline to prevent data leakage.
- Expanding candidate generation to recommend movies beyond observed user interactions.
- Comparing neural network predictions against simpler recommendation baselines.
- Adding ranking-based evaluation metrics.
- Developing an interactive recommendation interface.

## Project Status

Academic machine learning project with a corrected data pipeline and preserved original notebook. The revised notebook has **not yet been rerun end to end with TensorFlow**; evaluation results remain pending.

---
