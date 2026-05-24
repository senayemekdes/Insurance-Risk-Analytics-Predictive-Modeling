# AlphaCare Insurance Risk Analytics & Predictive Modeling

## Business Objective
Developed data-driven strategies to optimize marketing and implement risk-based pricing for car insurance in South Africa.

## Project Structure
- `data/` → Raw & versioned data (DVC)
- `notebooks/` → EDA, Hypothesis Testing, Modeling
- `src/` → Reusable Python modules
- `outputs/` → Results & visualizations

## Key Findings
- Overall Loss Ratio: ~X.XX%
- Gauteng shows elevated risk compared to Western Cape
- Vehicle Age and Province are among the strongest predictors of claim severity
- Random Forest performed best for claim severity prediction

## Technologies Used
- Python, Pandas, Scikit-learn, XGBoost
- DVC (Data Version Control)
- Git + GitHub Actions
- Statistical Testing (SciPy)

## How to Reproduce
```bash
dvc pull
pip install -r requirements.txt
jupyter notebook