# Ecommerce-eda-insights

# 1. Title & Description: E-Commerce Exploratory Data Analysis (EDA) Pipeline
This project is an Exploratory Data Analysis (EDA) portfolio piece designed to investigate customer transaction distributions, geographic purchasing tendencies, and dataset integrity checks using Python.

# 2. Problem Statement:
In real-world retail analytics, messy, missing, or synthetic data can severely damage company decision-making or break downstream machine learning models. The objective of this analysis is to evaluate an e-commerce retail dataset to uncover operational metrics, logistics preferences, and product trends while validating that the dataset's structural integrity is fit for strategic business forecasting.

# 3. Data Source: where the dataset comes from
- **Dataset:** Diversified E-Commerce Dataset (Subsampled to 1,000 rows to optimize git version control).
- **File Location:** `data/raw/diversified_ecommerce_dataset_small.csv`
- **Original Source Link:** [Kaggle Hub Dataset](https://www.kaggle.com/datasets/malaiarasugraj/e-commerce-dataset)

# 4. Methodology: Approach and Tools used
To build an environment capable of processing these data frames, the following tools and processing rules were applied:
- **Environment:** Google Colab notebook powered by Python.
- **Libraries:** `pandas` for core statistical structures, `matplotlib.pyplot` for rendering data visualizations, and `seaborn` for mapping contingency matrices.
- **Data Engineering:** Used `.head(1000)` to isolate a light, clean version of the workspace and compiled descriptive aggregations using `.groupby()` functions.

# 5. Key Findings: Main Insights
During the analytical process, a critical data audit insight was discovered:
- **Data Uniformity Anomaly:** Grouping categorical vectors like `Category` or `Customer Location` revealed exactly flat distributions (identical counts across all variables).
- **Logistical Matrix Symmetry:** Cross-tabulation matrices (`pd.crosstab`) cross-referencing shipping methods with customer locations showed uniform values (50-55 counts uniformly distributed) across all variations.
- **Strategic Interpretation:** This confirms the dataset is completely computer-generated (synthetic) using uniform random sampling. Spotting this distribution variance is a massive milestone in exploratory data operations.

# 6. Results: 
- **What the Code Showed:** When I used Python to count how many people used each shipping method across different locations, the numbers were exactly the same everywhere. Turning this into a color-coded chart (heatmap) proved that the data doesn't have real-world shopping patterns.
- **Where the Code Lives:** You can see all of my code, tables, and charts inside the `notebooks/eda_notebook.ipynb` file in this repository.
# 7. Conclusions:
- **What I Learned:** This project taught me that you must always check the shape and patterns of your data before trying to build any models. Because this dataset is just random computer-generated numbers, trying to use Machine Learning to predict prices or trends would completely fail (giving an accuracy score near 0%). 
- **Next Steps:** To make this project even better, the next step is to run these same Python cleaning and analysis scripts on real, web-scraped data from a real e-commerce store to see how actual human shopping habits look.
