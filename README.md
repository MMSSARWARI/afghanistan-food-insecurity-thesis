# Machine Learning Analysis of Household Food Insecurity and Vulnerability Profiles in Afghanistan

Code for the bachelor's thesis of Mohammad Mahdi Sarwari, Bachelor's degree in Economics with Data Science (L-33), University of Cassino and Southern Lazio, supervised by Prof. Ciro Russo, academic year 2025/2026.

## Notebooks

The analysis is in four Jupyter notebooks, which should be run in order.

| Notebook | Content |
|---|---|
| `01_cleaning.ipynb` | Loads DIEM Rounds 4 to 8, harmonizes the outcome (Food Consumption Group), keeps the structural predictors and handles missing values and skip logic. Saves one clean file per round. |
| `02_models.ipynb` | Multicollinearity checks, logistic regression, random forest and XGBoost, evaluation on the test set, permutation importance, SHAP values, the selection rule for the profiles, the province checks and the tuning check. |
| `03_profiles.ipynb` | Gower distance, clustering with partitioning around medoids, choice of the number of clusters, validation of the profiles, weighted shares and the milk component. |
| `04_rounds.ipynb` | Harmonization across rounds, weighted comparison of Rounds 4 to 8, the check of the Food Consumption Group thresholds and the transfer test from Round 6 to Round 8. |

## Data

The data are not included in this repository. They are the anonymized Data in Emergencies Monitoring (DIEM) household surveys for Afghanistan, available from the FAO Microdata Catalogue under its terms of use:

https://microdata.fao.org/index.php/catalog/Emergencies-Monitoring-Surveys

The notebooks expect these files in the same folder:

| File | Round |
|---|---|
| `data_anon.xlsx` | Round 4 |
| `anon_dfAFG_R5.xlsx` | Round 5 |
| `data_anon_AFG_R6.csv` | Round 6 |
| `anon_df_AFG_R7.csv` | Round 7 |
| `anon_dfAFG_R8.xlsx` | Round 8 |

## How to run

1. Install the packages: `pip install -r requirements.txt`
2. Put the data files in the same folder as the notebooks.
3. Run the notebooks in order, from `01_cleaning.ipynb` to `04_rounds.ipynb`, with Restart Kernel and Run All Cells.

All random steps use the seed 42. Small differences in the results can appear with other library versions; the thesis results were produced with pandas 3.0.3.
