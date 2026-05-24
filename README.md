# Insurance-Risk-Analytics-Predictive-Modeling
task -1 -done
Git, GitHub & Exploratory Data Analysis
Create a GitHub repository with a clear README.md, a Python .gitignore, and a requirements.txt.
Configure a GitHub Actions CI workflow that runs linting and tests on every push.
Create a branch named task-1 and commit your work at least three times a day with descriptive messages.
Perform EDA covering:
Data Summarization - descriptive statistics for numerical features (TotalPremium, TotalClaims, etc.), and a review of dtypes to confirm categorical, date, and numerical columns are correctly typed.
Data Quality Assessment - check for missing values and document handling strategy.
Univariate Analysis - histograms for numerical columns and bar charts for categorical columns.
Bivariate / Multivariate Analysis - relationships between TotalPremium and TotalClaims as a function of ZipCode, using scatter plots and correlation matrices.
Geographic Trends - compare cover type, premium, and auto make across provinces.
Outlier Detection - use box plots on key numerical features.
Answer the following guiding questions in your notebook:
What is the overall Loss Ratio for the portfolio? How does it vary by Province, VehicleType, and Gender?
What are the distributions of key financial variables? Are there outliers in TotalClaims or CustomValueEstimate that could skew analysis?
Are there temporal trends? Did claim frequency or severity change over the 18-month period?
Which vehicle makes/models are associated with the highest and lowest claim amounts?
Produce at least 3 creative and well-designed plots that capture the key insights from your EDA.

task-2 done
Objective: Establish a reproducible and auditable data pipeline using DVC, a standard practice in regulated industries where every analysis or model result must be reproducible at any time for auditing, regulatory compliance, or debugging.

Instructions:

Merge task-1 into main via a Pull Request, then create a new branch task-2.
Install DVC: pip install dvc.
Initialize DVC in the project: dvc init.
Set up local remote storage:
Create a storage directory outside the project: mkdir /path/to/local/storage.
Add it as a DVC remote: dvc remote add -d localstorage /path/to/local/storage.
Track the dataset with dvc add data/insurance_data.csv and commit the resulting .dvc files to Git.
Create at least two versions of the data (e.g., raw and cleaned) and push to the local remote with dvc push.

task-3 done
## Business Recommendations
- Although not statistically significant, Gauteng shows elevated risk → Consider province-specific loading.
- No strong evidence to differentiate pricing by gender at this stage.
- Further analysis on Zip Codes and Vehicle segments recommended.
task-4- done
Average Current Premium (CalculatedPremiumPerTerm): R 117.88
Average Suggested Premium (Risk-Based): R 29483.11

================================================================================
                  FINAL BUSINESS RECOMMENDATIONS
================================================================================

1. **Implement Risk-Based Pricing**:
   - Use predicted claim severity + probability of claim to calculate dynamic premiums.
   - Apply higher loading for high-risk segments (e.g., Gauteng, older vehicles).

2. **Target Low-Risk Segments**:
   - Focus marketing on low-risk provinces and vehicle types to improve overall Loss Ratio.

3. **Product Adjustments**:
   - Offer lower premiums / higher excesses for low-risk profiles.
   - Introduce telematics (TrackingDevice) discounts.

4. **Next Steps**:
   - Deploy the Random Forest model in production.
   - A/B test new pricing tiers.
   - Continuously retrain model with new data.
