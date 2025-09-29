# csc172-data-mining-maglasang

## Project Structure

```
csc172-data-cleaning-maglasang/
│── data/
│   ├── raw_dataset.csv
│   ├── cleaned_dataset.csv
│
│── notebooks/
│   ├── data_cleaning.ipynb
│
│── README.md
```

## Dataset

* **Raw dataset:** `data/raw_dataset.csv` (original House Prices dataset).
* **Cleaned dataset:** `data/cleaned_dataset.csv` (after preprocessing).

## Steps Performed

1. Loaded the dataset and performed exploratory checks:

   * `df.info()`
   * `df.describe()`
   * Missing values check
   * Duplicate check
2. Cleaning steps applied:

   * Missing value handling:

     * Numerical → filled with median
     * Categorical → filled with mode
   * Duplicate removal
   * Standardized categorical formats (e.g., capitalization, trimmed spaces)
   * Outlier treatment (capped at 1st and 99th percentile)
3. Saved cleaned dataset to `data/cleaned_dataset.csv`.

## Before and After Snapshots

* **Shape before:** (1460, 81)
* **Shape after:** (1460, 81)
* **Missing values before:** Several (e.g., `LotFrontage: 259`, `Alley: 1369`)
* **Missing values after:** 0
* **Duplicates before/after:** 0

## AI Assistant Usage

As required, I used an AI assistant (ChatGPT) to guide the cleaning pipeline.

**Prompt given:**

```
Use Python (Pandas). Use an AI assistant at least once and include the prompt & response in README.

Load the raw dataset and perform exploratory checks 
df.info()
df.describe() 
missing values
duplicates
Apply cleaning steps: 
missing value handling
duplicate removal
standardize formats
detect/treat outliers
Include before and after snapshots of the following:
shapes
sample rows
summary statistics
Save cleaned dataset as data/cleaned_dataset.csv.

do all these to csv file
```

**AI Assistant Response (summary):**

* Loaded dataset with Pandas
* Performed exploratory checks (`df.info()`, `df.describe()`, missing values, duplicates)
* Suggested two options for handling missing data:

  1. Keep all columns and impute missing values
  2. Drop high-missing columns
* Implemented Option 1 (keep all columns, fill missing with median/mode)
* Standardized categorical formats
* Capped numeric outliers at 1st and 99th percentiles
* Exported final dataset to `data/cleaned_dataset.csv`

---

## How to Run

1. Open `notebooks/data_cleaning.ipynb`
2. Run all cells to reproduce cleaning process
3. Cleaned dataset will be saved at `data/cleaned_dataset.csv`

## Drive Link For the Video Presentation

https://drive.google.com/drive/folders/1bAXRXrY2uESxAeQt1JE8gsYEyHrKrSjj?usp=sharing

