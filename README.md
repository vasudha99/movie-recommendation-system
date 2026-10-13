# Intelligent Movie Recommendation System Using Multi-Layer Perceptron (MLP)

**Python | TensorFlow/Keras | Deep Learning | Recommendation Systems**

This project develops an intelligent movie recommendation system that predicts user ratings and generates personalised movie suggestions. It combines user–movie interactions, movie metadata and a Multi-Layer Perceptron (MLP) with user and movie embedding layers.

The project was developed as part of the Artificial Intelligence (CP70069E) module at the University of West London.

## Project Overview

The recommendation system uses historical ratings and movie attributes to understand user preferences. For existing users, it generates personalised suggestions based on predicted ratings and genre preferences. For new users, it provides recommendations using highly rated and popular movies.

## Technologies

- **Python** for implementation
- **TensorFlow and Keras** for the neural network
- **Pandas and NumPy** for data preparation
- **Scikit-learn** for encoding, scaling, data splitting and evaluation
- **Matplotlib and Seaborn** for exploratory analysis and training visualisations
- **Google Colab / Jupyter Notebook** for development

## Dataset

Source: [The Movies Dataset on Kaggle](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)

The original project uses:
- `ratings_small.csv`: User IDs, movie IDs and ratings
- `movies_metadata.csv`: Movie titles, genres, vote averages, vote counts, budgets, revenues and runtimes

## Methodology

1. **Data preprocessing:** Parse genres, handle missing values, convert data types and prepare ratings and metadata.
2. **Exploratory data analysis:** Explore rating distributions, user activity and movie popularity.
3. **Feature engineering:** Encode user/movie IDs and genres, and scale numerical movie attributes.
4. **MLP architecture:** Use 50-dimensional user and movie embeddings, followed by dense layers of 128, 64 and 32 neurons with ReLU activations.
5. **Model training:** Train with Adam optimisation, mean squared error loss, regularisation and early stopping.
6. **Evaluation:** Assess predicted ratings using MAE and MSE, with training and validation visualisations.
7. **Recommendations:** Generate recommendations for existing users and popularity-based suggestions for new users.

## Results

The results reported in the original academic project are:

| Metric | Result |
|---|---:|
| Test Mean Absolute Error (MAE) | **0.7344** |
| Test Mean Squared Error (MSE) | **0.8811** |

The academic report also includes rating-distribution graphs, training and validation curves, and examples of recommendations for existing and new users.

## Project Files

- [Movie recommendation notebook](movie_recommendation.ipynb): Original project code and explanations
- [Original notebook archive](archive/movie_recommendation_original.ipynb): Preserved original notebook
- [Requirements](requirements.txt): Python dependencies
- `data/`: Location for downloaded datasets (dataset files are not stored in this repository)

## Running the Project

1. Download `ratings_small.csv` and `movies_metadata.csv` from the Kaggle dataset above.
2. Open the notebook in Google Colab.
3. Use the dataset paths configured in the notebook for your Colab environment.
4. Run the cells in order to explore the data, train the MLP and generate recommendations.

## Skills Demonstrated

Deep learning, neural network modelling, recommendation systems, embeddings, exploratory data analysis, feature engineering, model evaluation and Python data science.
