# Intelligent Movie Recommendation System (MLP)

A Jupyter Notebook project that predicts user movie ratings using TensorFlow/Keras user and movie embeddings, numerical movie metadata, and a multi-layer perceptron. The notebook also contains a recommendation function using predicted ratings and genre preferences.

## Tools
Python, Pandas, NumPy, scikit-learn, TensorFlow/Keras, Matplotlib, Seaborn.

## Data
The notebook expects `data/ratings_small.csv` and `data/movies_metadata.csv` from **The Movies Dataset** (Kaggle, `rounakbanik/the-movies-dataset`). Download these files from the dataset's source and place them in the `data/` folder. The CSV files are intentionally excluded from this repository draft; check source licensing before redistribution.

## Saved results from original coursework run
- Test MAE: **0.7344**
- Test MSE: **0.8811**

These numbers are taken from the original notebook's saved output. **They have not been reproduced in this cleaned draft.**

## Run
1. Create a Python environment and install dependencies: `pip install -r requirements.txt`
2. Download the two CSV files and put them in `data/`.
3. Open `movie_recommendation.ipynb` in Jupyter or VS Code and run cells in order.

## Known limitations / improvements needed
- The original notebook performs scaling and encoding before train/test splitting; refactor preprocessing to fit on training data only before treating the reported metrics as a leakage-free benchmark.
- The recommendation function predicts using rows from the observed interactions, not a complete user–movie candidate grid. Review this logic before describing it as a production-ready recommender.
- Movie IDs and metadata should be checked for join consistency.
- Notebook outputs were cleared for a smaller, cleaner repository; rerun to regenerate plots.
- The draft has not been executed end-to-end in this environment.

## Project status
**Academic portfolio draft — requires validation before public promotion.**
