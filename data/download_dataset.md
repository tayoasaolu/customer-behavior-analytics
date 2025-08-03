# Dataset Information and Download Instructions

## Overview
This project uses the [Online Retail UCI Dataset from Kaggle](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci) for customer behavior analysis. It contains ~500,000 rows of transactional data from an online retail store, including columns like `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, and `Country`.

- **Why this dataset?** It's open-source, rich in transactional details, and perfect for RFM (Recency, Frequency, Monetary) analysis, clustering, and regression to segment customers and predict retention.
- **License**: CC BY 4.0 (Attribution required – cite the source in your work).
- **File Format**: Excel (online_retail_II.xlsx) or CSV (convert if needed).

Do **not** upload the full dataset to this repo to avoid size limits and bloat. Instead, follow the steps below to download and prepare it locally.

## Download Steps
1. **Go to Kaggle**: Visit the [dataset page](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci).
2. **Sign In/Register**: Create a free Kaggle account if you don't have one.
3. **Download**: Click "Download" to get the ZIP file. Extract the Excel file (`online_retail_II.xlsx`).
4. **Rename and Place**: Optionally rename to `online_retail.csv` (convert to CSV using Excel or Pandas for easier loading) and place it in this `data/` folder locally.

## Data Preparation
To use with the Jupyter notebook:
- **Load in Python**: In `../notebooks/analysis.ipynb`, use Pandas to read the file:
  ```python
  import pandas as pd
  df = pd.read_excel('data/online_retail_II.xlsx')  # Or .csv if converted
  ```
- **Cleaning Tips**:
  - Handle missing values (e.g., drop rows with null `CustomerID`).
  - Convert `InvoiceDate` to datetime: `df['InvoiceDate'] = pd.to_datetime(df['InvoiceDate'])`.
  - Compute RFM metrics as shown in the notebook.
- **Size Considerations**: The dataset is large; for testing, sample it with `df.sample(frac=0.1)`.

## Exported Files
- The notebook may generate processed CSVs here (e.g., `rfm_data.csv` after calculations) for reuse.
- Visuals are saved to `../visuals/`.

If you encounter issues with data types or columns, refer to the Kaggle dataset description for the full schema. For alternatives, consider the [E-commerce Customer Churn Dataset](https://www.kaggle.com/datasets/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction).
```
2. **Why this file?** It ensures the project is reproducible without bloating the repo. Users can easily get the data and jump into the analysis.

Once you've added this, reply with "next file" (or any questions/feedback), and I'll generate the next one: **`notebooks/analysis.ipynb`** (the Jupyter Notebook file with the core Python code for clustering, regression, and visualizations). Note: Since .ipynb is a JSON-based file, I'll provide it as JSON content that you can paste into a new .ipynb file (or use Jupyter to create it). 🚀
