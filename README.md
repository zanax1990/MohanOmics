# 🧬 MohanOmics Analyzer

![Python Version](https://img.shields.io/badge/python-3.9%2B-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-v1.38.0-FF4B4B)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-v3.5%20Golden%20Match-gold)

**MohanOmics Analyzer** is a robust, interactive bioinformatics dashboard designed for the end-to-end analysis of label-free DIA (Data-Independent Acquisition) proteomics data. Built with Python and Streamlit, it streamlines the workflow from raw export processing to biological pathway discovery.

> **Note:** Optimized for mouse datasets (*Mus musculus*), leveraging specific logic for zero-variance handling and AI-based imputation.

## 🚀 Key Features

### 1. 🧹 Automated Quality Control
- **Real-time Filtering:** Adjust Q-Value thresholds dynamically.
- **Data Cleaning:** Option to remove single-hit proteins for higher confidence.
- **Pivot Logic:** Automatically transforms long-format reports into expression matrices.

### 2. 🤖 AI-Driven Imputation
- **KNN Imputation:** Uses *k-Nearest Neighbors* to intelligently fill missing values based on protein expression patterns.
- **Fallback Methods:** Options for "Min Value" or "Zero Fill" for comparison.
- **Log2 Transformation:** Handles data normalization with automatic infinity protection.

### 3. 📊 Advanced Visualization
- **Interactive PCA:** 2D Principal Component Analysis with dynamic grouping.
- **Correlation Heatmaps:** Visualizes sample-to-sample reproducibility.
- **Volcano Plots:** Interactive scatter plots with adjustable Log2FC and P-value cutoffs.

### 4. 🧮 Statistical Rigor
- **Vectorized Welch’s T-Test:** Custom implementation that matches R-language precision.
- **Edge Case Handling:** Specifically handles "Presence/Absence" scenarios where variance is zero in one or both groups (Golden Match logic).

### 5. 🧬 Biological Insight
- **Pathway Enrichment:** Direct integration with `g:Profiler` API.
- **Gene Ontology & KEGG:** Automatically fetches enriched terms for Upregulated vs. Downregulated sets.

---

## 🛠 Installation

Clone the repository and install the dependencies:

```bash
git clone [https://github.com/yourusername/MohanOmics.git](https://github.com/yourusername/MohanOmics.git)
cd MohanOmics
pip install -r requirements.txt

UsageRun the application locally:Bashstreamlit run app.py
Once running, the dashboard will open in your default browser at http://localhost:8501.📂 Input Data FormatThe tool is designed to parse Spectronaut DIApasef style reports (CSV or TSV). Ensure your input file contains the following columns:Column NameDescriptionPG.ProteinAccessionsUniProt Accession IDPG.GenesGene NamePG.QuantityRaw Intensity/QuantityR.ConditionExperimental Condition (Group)R.ReplicateReplicate NumberPG.QValue (Run-Wise)Quality Score for filteringPG.IsSingleHitBoolean flag for single peptide hits


