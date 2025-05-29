# Persistent representation of a prior schema in the orbitofrontal cortex facilitates learning of a conflicting schema – Analysis Code

This repository contains the code for the manuscript **"Persistent representation of a prior schema in the orbitofrontal cortex facilitates learning of a conflicting schema"**, including all steps to reproduce the main figures.

---

## 📁 Project Structure

- `All_dataset/`: 
  - Contains preprocessed session-level data (`all_data_<session_name>.pkl`)
  - Also includes UMAP result files integrating across sessions
  - Contains 3 hypothesized confusion matrix templates used for model comparisons

	Due to GitHub storage limits, the full dataset (~7 GB) is hosted externally.
	[🔗 Download All_dataset.zip from Zenodo](https://doi.org/10.5281/zenodo.15548209)


- `Persistent-representation-of-a-prior-schema.ipynb`: Main Jupyter notebook for generating figures and running analyses.

- `requirements.txt`: Required Python libraries.


---

## 🖥️ 1. System Requirements

### Software Dependencies
- Python 3.9
- Jupyter Notebook
- Required Python packages (see `requirements.txt`), including:
  - numpy
  - pandas
  - matplotlib
  - seaborn
  - scikit-learn
  - umap-learn
  - pickle
  - joblib

### Tested On
- macOS Monterey 12.6
- Ubuntu 20.04
- Windows 10

### Non-Standard Hardware
- No non-standard hardware is required. Analyses were run on standard desktop and laptop computers.

---

## 🧠 Data Contents

### Session Dictionaries (`all_data_<session_name>.pkl`)

Each file in `All_dataset/` is a pickled dictionary with:

```python
dict_keys([
    'session_name',
    'session_title',
    'spikeTime',
    'Analysis_table_f',
    'behave_dict',
    'PETH',
    'Trials',
    'V_pca',
    'exp_var',
    'exp_var_epochs',
    'cm_similarity_pca',
    'cm_similarity_lda',
    'cm_similarity_pca_epochs',
    'result_dict_Zeta',
    'responsivness',
    'z_score_all_trials',
    'SVM',
    'SVM_pca',
    'SVM_no_selective',
    'SVM_no_cdnm',
    'SVM_no_disc',
    'SVM2'
])
```

Key elements:
- **`Analysis_table_f`**: DataFrame of behavioral events per trial
- **`spikeTime`**: Array of spike timestamps per unit

---

### 🔍 UMAP Analysis Files

Also located in `All_dataset/`, these files contain results from UMAP projections that integrate neural data across sessions and animals. These are used to generate population-level similarity embeddings shown in **Figure 5**.

---

### 🧩 Hypothesized Templates

Three separate files in `All_dataset/` represent theoretical confusion matrix structures based on different rule types:

- **Non-match rule template**
- **Cue-identity rule template**
- **Combined rule template**

These are used for model comparison in Figure 6, assessing which behavioral rule best matches the neural similarity structure.

---

## ✅ Getting Started

### 1. Install Dependencies 

```bash
pip install -r requirements.txt
```

Or with conda:

```bash
conda create -n schema_env python=3.9
conda activate schema_env
pip install -r requirements.txt
```
### Typical Install Time
Approximately 2–5 minutes on a standard desktop with an internet connection.

### 2. Download and unzip the All_dataset.zip file
	[🔗 Download All_dataset.zip from Zenodo](https://doi.org/10.5281/zenodo.15548209)
	After downloading, unzip the `All_dataset.zip` file into the root of the repository 		before running the notebook.

### 3. Run the Notebook

```bash
jupyter notebook Persistent-representation-of-a-prior-schema.ipynb
```

Progress through the notebook cells to regenerate the analyses and manuscript figures. 

### Estimated Run Time
- Full notebook execution takes about 7–15 minutes on a typical desktop/laptop.

---

### Reproducibility
All data and code necessary to reproduce the manuscript figures are included. Analyses apply uniformly across all sessions, with no manual parameter tuning.


## 📄 License

This project is released for academic and research use only.

---

## 📬 Contact

For questions or collaboration inquiries, please contact: idomaor@gmail.com
