MohanOmics: AI-Driven Proteomics Analyzer

Interactive Streamlit application for QC, imputation, PCA, differential expression, and pathway enrichment in proteomics datasets.

📌 Overview

MohanOmics Analyzer is a fully interactive, end-to-end analysis suite for label-free DIA proteomics data.
It supports:

Automated QC of protein groups

AI-based missing value imputation (KNN)

PCA and correlation heatmaps

Vectorized Welch’s t-test with log2FC

Volcano plots with significance filters

GO Biological Process & KEGG pathway enrichment via g:Profiler

The app is optimized for mouse datasets (mmusculus) but works with any organism supported by g:Profiler.

🚀 Features
1. Data Import

Accepts .csv and .txt DIApasef / Spectronaut-style reports

Automatically handles column pivots into protein expression matrices

2. Quality Control

Apply real-time filtering:

Q-value thresholding

Removal of single-hit proteins

3. AI-Powered Imputation

KNN-based imputation for missing values

Optional Min-Value and Zero-Fill alternatives

Log2 transformation with automatic ∞ handling

4. PCA & Heatmaps

Two-component PCA with sample grouping

Correlation matrix heatmap using Plotly

5. Differential Expression

Fully vectorized Welch's t-test (R-compatible behaviors)

Log2 fold change computation

Volcano plot with configurable cutoffs

Exportable table of significant proteins

6. Pathway Analysis

GO:BP and KEGG enrichment

Horizontal bar plots of top pathways

Separate analysis for upregulated and downregulated genes

🛠 Installation
git clone https://github.com/yourusername/MohanOmics.git
cd MohanOmics
pip install -r requirements.txt

▶️ Run the App
streamlit run app.py

📁 Project Structure
MohanOmics/
│── app.py                 # Main Streamlit application
│── requirements.txt       # Python dependencies
│── README.md              # Project documentation

📦 Dependencies

streamlit

pandas

numpy

scipy

scikit-learn

plotly

gprofiler-official

🧬 Example Dataset

The app supports Spectronaut DIApasef report exports with columns:

PG.ProteinAccessions

PG.Genes

PG.Quantity

R.Condition

R.Replicate

PG.QValue (Run-Wise)

PG.IsSingleHit

📸 App Preview



👨‍🔬 Author

Developed by Jahanbakhsh Ghasemi
University of Connecticut, 2025
