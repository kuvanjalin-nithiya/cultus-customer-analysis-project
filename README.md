# Exploratory Analysis of Synthetic Customer Spending Data

**Project type:** Data exploration / EDA (synthetic dataset)  
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn

---

## Project Overview
This repository contains a reproducible exploratory data analysis (EDA) pipeline that generates a synthetic customer spending dataset (≥500 records) and produces the required visualizations and a short text summary. The goal is to demonstrate foundational data science skills: data generation, cleaning, visualization, and concise interpretation.

---

## 1. Project Objectives (Deliverable)
1. Generate or load a dataset containing at least 500 records with numerical features (`Age`, `Income`, `SpendingScore`) and one categorical feature (`Segment`).
2. Perform initial data cleaning and summary statistics (mean, median, std, quartiles).
3. Create three required visualizations:
   - Histogram (distribution of `SpendingScore`)
   - Box plot (identify outliers in `Income`)
   - Scatter plot (relationship between `Age` and `SpendingScore`)
4. Analyze the relationship between the categorical feature (`Segment`) and a numerical feature (`Income`).
5. Provide a concise text-based analysis detailing steps taken, descriptive statistics, and main insights.

---

## 2. Files in this repository
```
project/
├── exploratory_synthetic_spending.ipynb    # Jupyter notebook with full pipeline (recommended)
├── generate_and_eda.py                     # Script version of the notebook (optional)
├── synthetic_spending_data.csv             # (If generated, saved here)
├── plots/
│   ├── histogram_spending_score.png
│   ├── boxplot_income.png
│   └── scatter_age_spending.png
├── README.md
└── requirements.txt
```

---

## 3. Dataset Overview
The synthetic dataset contains:
- **Age** (numerical): 18–70
- **Income** (numerical): annual income in local currency
- **SpendingScore** (numerical): 1–100 customer spending score
- **Segment** (categorical): `Low`, `Middle`, `High`

A synthetic dataset is generated using NumPy with realistic distributions and saved as `synthetic_spending_data.csv`.

---

## 4. Feature Engineering (Rationale)
Three simple but meaningful features / checks used:
- **Age** — demographic grouping for segmentation of behavior.
- **Income** — identifies high/low purchasing power and outliers.
- **SpendingScore** — proxy for recent spending activity or engagement.

These variables are chosen because they are commonly used in customer segmentation and basic risk/profit analysis.

---

## 5. How the pipeline works (high-level)
1. **Generate dataset** (or load provided CSV).
2. **Inspect** for missing values and types.
3. **Compute summary statistics**: mean, median, std, min, max, quartiles.
4. **Visualize**:
   - Histogram of `SpendingScore` (distribution & skewness)
   - Box plot of `Income` (outliers detection)
   - Scatter plot `Age` vs `SpendingScore` (relationship)
5. **Group analysis**: compute average `Income` per `Segment`.
6. **Save** plots to `/plots/` and optionally export dataset CSV.

---

## 6. How to run (local / Colab)
### Option A — Jupyter Notebook (recommended)
1. Clone repo:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
2. Create environment & install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate     # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. Open the notebook:
   ```bash
   jupyter notebook exploratory_synthetic_spending.ipynb
   ```
4. Run cells sequentially. Plots will be saved into `/plots/`.

### Option B — Google Colab
1. Upload the notebook `exploratory_synthetic_spending.ipynb` to Colab or open from GitHub.
2. Run all cells. If you want to download generated files, use:
   ```python
   from google.colab import files
   files.download('synthetic_spending_data.csv')
   files.download('plots/histogram_spending_score.png')
   ```
3. After running, download the `/plots/` images and the CSV for submission.

---

## 7. Expected outputs (deliverables)
- `synthetic_spending_data.csv` (or link to dataset used)
- `/plots/histogram_spending_score.png`
- `/plots/boxplot_income.png`
- `/plots/scatter_age_spending.png`
- A short text summary (included in notebook README cell and notebook markdown) describing:
  - Dataset size and key descriptive stats
  - Main insights from plots
  - A short conclusion with 2–3 actionable insights

---

## 8. Example Insights (what to write in the text summary)
- Spending Score shows a moderate spread (no extreme skew) — marketing can target middle decile for upsell.
- Income has outliers — verify extreme values or cap if modelling.
- Weak correlation between Age and SpendingScore — age alone is not a strong predictor of spending.
- Average Income per `Segment` shows `High` segment with significantly larger mean income — prioritize personalized campaigns.

---

## 9. Requirements (`requirements.txt`)
A minimal `requirements.txt` for reproducibility:
```
numpy>=1.21
pandas>=1.4
matplotlib>=3.5
seaborn>=0.12
jupyterlab          # optional, for notebook execution
```

(If you used Colab, add any extra libs used in the notebook.)

---

## 10. Notes & Good Practices
- Keep plots in `/plots/` and version-control the notebook and scripts.
- Do **not** include large binary files in repo; push images and CSV only if small. Use `.gitignore` for bulky data.
- Write clear markdown cells in the notebook — reviewers evaluate both code and the written interpretation.
- If you used synthetic data, explicitly state that in the README (we did) and ensure the data generation seed is fixed for reproducibility (`np.random.seed(42)`).

---

## 11. Contact
If you need help or want the instructor to re-run the notebook, include your contact or a short note in the submission text field.

---

**End —** Copy the notebook code and this README into your repository. Run everything once locally/Colab, confirm plots are saved under `/plots/`, then push to GitHub and paste the GitHub URL in the Cultus submission box along with a short explanatory paragraph.
