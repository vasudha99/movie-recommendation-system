# Dataset Validation

The original project uses `ratings_small.csv` (100,004 ratings) and `movies_metadata.csv` from Kaggle's The Movies Dataset.

## Verified local dataset audit (13 October 2026)

- Ratings: **100,004**, with **0 missing values** across the four ratings columns and **0 duplicate user–movie pairs**.
- Distinct rated movies: **9,066**.
- Metadata rows: **45,466**.
- **44,989** ratings match a metadata ID through the notebook's direct `ratings.movieId = movies.id` merge; **55,015** ratings do not.
- Only **2,830** distinct rated movie IDs match metadata IDs directly.

## Important modelling issue

The two files do not use interchangeable movie identifiers. Directly merging `ratings_small.movieId` with `movies_metadata.id` discards data and may associate ratings with the wrong titles. **Do not treat that merge as validated.** Use the MovieLens-to-TMDb mapping in `links_small.csv` (and inspect coverage) before incorporating metadata, or train the rating-prediction model on `ratings_small.csv` alone.

The existing notebook also fits some preprocessing before the train/test split. That needs correction to avoid data leakage.

The README's MAE/MSE are historical notebook outputs, **not independently reproduced**. TensorFlow training has not yet been rerun in a verified environment.

## Next validation steps

1. Add `links_small.csv` from the same dataset if metadata is required.
2. Split ratings into training, validation, and test sets before fitting encoders and scalers.
3. Fit preprocessing only on training data; handle unseen IDs explicitly.
4. Compare against a mean-rating baseline.
5. Evaluate on a held-out test set and only then update the README with reproduced metrics.
6. Test that recommendations exclude already-rated movies and rank eligible candidates.
