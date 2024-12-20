# Breast Cancer Immune Repertoire Analysis

This project involves the analysis of immune repertoire data obtained from the blood samples of healthy donors and breast cancer patients. 
The immune repertoire data includes T-cell receptor alpha (TRA) and beta (TRB) sequences obtained through Repertoire Sequencing (Rep-Seq). 
The analysis includes data preprocessing, feature filtering, and machine learning for classification.

## Data Collection and Processing

1. **Blood Collection:**
   - Blood samples were collected from healthy donors and breast cancer patients.

2. **Repertoire Sequencing (Rep-Seq):**
   - Repertoire Sequencing was performed on the collected blood samples to obtain TRA and TRB sequences.

3. **Data Processing with MiXCR:**
   - The obtained raw sequencing data went through the MiXCR pipeline for processing.

4. **Concatenation of TRA and TRB Files:**
   - The processed TRA and TRB files were concatenated for further analysis.

## Data Analysis

### Immunarch Analysis

- **immunarch_analysis.Rmd:**
  - This R Markdown script performs subsampling on the concatenated data and conducts basic analyses using the `immunarch` package.
- **create_df.Rmd:**
  - This R Markdown script creates a dataframe of features x samples from the subsampled data.
- **multiple_subsamplings.Rmd:**
  - This R Markdown script creates a dataframe of features x samples from 4 different subsamplings of the data.

## Machine Learning

- **ML_breast.ipynb** 
  - This Jupyter Notebook contain Python scripts for machine learning.
  - The data resulting from `create_df.Rmd` and `multiple_subsamplings.Rmd` are processed through this notebook.
  - Machine learning algorithms are applied for classification using the `atom` package.

## Usage

- The analysis can be reproduced by following the steps outlined in each analysis script.
- Ensure that the required dependencies (such as R packages and Python libraries) are installed.
- The project was developed and tested with the following package versions:
   - Python: 3.8.13
   - NumPy: 1.21.2
   - Pandas: 1.4.1
   - Scikit-learn: 1.0.2
   - atom-ml: 4.12.0
- To reproduce the Python environment, `conda env create -f environment.yml`.

## Data Availability

- The raw data is available on Zenodo.
