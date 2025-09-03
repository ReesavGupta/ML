## Files
- `titanic.ipynb` — the main notebook with labeled tasks (Part A–C).
- `train_cleaned.csv` — exported cleaned training data (created by the notebook).
- (Optional) `test.csv` — the Kaggle test file if you want to mirror cleaning steps.
- `README.md` — this file.

## Data
Download `train.csv` (and optionally `test.csv`) from the Kaggle Titanic competition page and place them in the same folder as the notebook.

## Approach (edit this)
1. **Inspection:** Loaded the dataset, checked shape, dtypes, and head.
2. **Summary & counts:** Built a column summary and frequency tables for key categoricals.
3. **Cleaning:** Imputed missing `Age` by `(Pclass, Gender)` median; filled missing `Embarked` with mode.
4. **Feature engineering:** Extracted `Title` from `Name`, computed `FamilySize`, `IsAlone`, `CabinDeck`, and `TicketCount`.
5. **Outliers:** Capped `Fare` at the 99th percentile.
6. **Aggregation & pivots:** Explored survival patterns by `Gender`, `Pclass`, `IsAlone`, `AgeGroup`.
7. **Pipeline:** Built a small preprocessing pipeline and exported `train_cleaned.csv`.
8. **Storytelling:** Used up to three features to argue which combinations most associate with survival.

## Assumptions / Choices (edit this)
- Used `Sex` → `Gender` alias for compatibility with the assignment wording.
- Median imputation chosen for robustness to skew.
- Fare capping at 99th percentile to reduce outlier influence.

## How to run
Open the notebook and run cells top-to-bottom. Ensure `train.csv` is present in the same directory. The pipeline section will export `train_cleaned.csv`.