# Midterm — Members 2 & 3 (proposed allocation)

The original repository contained a preprocessing notebook and two aggregated RFM CSV files, but **no assignment specifying Member 2 / Member 3 responsibilities**. Therefore these deliverables use a proposed division; adapt headings to the instructor's actual task list.

## Member 2 — EDA and RFM segmentation
Open `notebooks/member2_midterm_eda_rfm.ipynb`. Deliverables: descriptive statistics, RFM distributions, Spearman correlations, RFM 1–5 scores, business-oriented customer segmentation, three charts, CSV summaries.

## Member 3 — clustering and churn-risk proxy
Open `notebooks/member3_midterm_clustering_churn.ipynb`. Deliverables: K-means K selection (2–7) using sample silhouette, PCA scatter, cluster profiles, and descriptive recency-based inactivity flags with exported CSVs. **Churn risk is only a heuristic, not prediction of labeled churn.**

## Run
From the `notebooks/` folder launch Jupyter and run all cells of each notebook. Packages: `pandas numpy matplotlib scikit-learn notebook` (notebook package optional in VS Code). Dataset paths work from repository root or `notebooks/`. Figures/CSVs save in repository `outputs/` if run from the notebook folder or repository root.

Source dataset: the existing `notebooks/dataset/rfm_raw.csv` and `rfm_scaled.csv`, each containing 5,878 customers. The original `preprocessing.ipynb` expects `online_retail_II.csv` extracted and placed in the working directory; the new notebooks **do not need to rerun preprocessing**.

Caveats: original preprocessing removes returns, missing Customer IDs, and invalid quantity/price; Monetary is gross positive spending, not net sales. RFM is aggregated over the full historical period; no independently observed churn label is supplied.
