# Visualizations Guide

## Overview
This folder is for storing visualizations generated from the analysis in `../notebooks/analysis.ipynb`. The notebook saves plots automatically (e.g., to `clusters.png` and `regression_plot.png`) using Matplotlib/Seaborn.

- **Why this folder?** It keeps images separate for easy reference in the README.md or presentations.
- **File Types**: PNG or JPEG for plots. Keep files under 10 MB each to avoid GitHub limits.

Do **not** commit large batches of images if unnecessary—use this guide to generate them locally.

## Generating Visuals
1. **Run the Notebook**: Open `../notebooks/analysis.ipynb` in Jupyter and execute all cells (after loading the dataset).
   - Key plots:
     - Customer Segments: Scatter plot of Frequency vs. Monetary by Cluster.
     - Regression Results: Scatter of Actual vs. Predicted Monetary.
   - Saves to: `visuals/clusters.png` and `visuals/regression_plot.png`.

2. **Custom Plots** (Optional):
   - Add in notebook:
     ```python
     # Example: RFM Distribution
     sns.pairplot(rfm[['Recency', 'Frequency', 'Monetary']])
     plt.savefig('visuals/rfm_distribution.png')
     plt.show()
     ```
   - Run and save new plots here.

## Adding to Repo
- **Upload Images**: After generating, use GitHub's "Add file" > "Upload files" to add PNGs to this `visuals/` folder.
- **Reference in README**: Update `../README.md` with paths like `![Clusters](visuals/clusters.png)`.
- **Tips**:
  - Compress images if large (e.g., using tools like TinyPNG).
  - For dynamic demos, consider GIFs (e.g., animated cluster exploration).
  - If plots don't generate, check dependencies in `../requirements.txt`.

Example Visuals (placeholders):
- `clusters.png`: Shows 4 customer segments.
- `regression_plot.png`: Demonstrates model fit with ~90% accuracy.

These visuals highlight key insights, such as high-value customer groups for retention strategies.
