# MIT-BIH Atrial Fibrillation Detection Project


<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/2/2e/Electrocardiogram.png" alt="ECG Example" width="400"/>
  <br><br>
  <img src="https://raw.githubusercontent.com/mitdbg/ecg-figures/main/afib_example.png" alt="AFib Example" width="400"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Notebook-.ipynb-blue?style=for-the-badge&logo=jupyter"/>
  <img src="https://img.shields.io/badge/Deep%20Learning-1D%20CNN-orange?style=for-the-badge&logo=tensorflow"/>
  <img src="https://img.shields.io/badge/ML-Random%20Forest-green?style=for-the-badge&logo=scikit-learn"/>
  <img src="https://img.shields.io/badge/Data-MIT--BIH%20AFDB-purple?style=for-the-badge&logo=databricks"/>
</p>

---

## 📚 Overview
This project analyzes the MIT-BIH Atrial Fibrillation Database to detect atrial fibrillation (AF) from ECG signals using both classical machine learning and deep learning (1D CNN) approaches. All code and analysis are in the Jupyter notebook `427_Project (3).ipynb`.

---

## 🖼️ ECG Signal Examples

| Normal ECG | Atrial Fibrillation ECG |
|:----------:|:----------------------:|
| ![Normal ECG](https://upload.wikimedia.org/wikipedia/commons/2/2e/Electrocardiogram.png) | ![Atrial Fibrillation ECG](https://raw.githubusercontent.com/mitdbg/ecg-figures/main/afib_example.png) |

<p align="center">
  <b>Normal ECG</b> &nbsp;&nbsp;&nbsp;&nbsp; <b style="color:#b71c1c;">Atrial Fibrillation</b>
</p>

---

## 🗂️ Project Structure
```
├── 427_Project (3).ipynb      # Main Jupyter notebook (all code & analysis)
├── README.md                  # This file
├── mit-bih-atrial-fibrillation-database-1.0.0.zip  # Raw dataset (ignored by git)
├── afdb/                      # Extracted ECG files (ignored by git)
├── processed_patient_split/    # Preprocessed data (ignored by git)
```

---

## 🚀 Workflow Summary

1. **Install dependencies**: `scikit-learn`, `wfdb`, `tqdm`, `tensorflow`, etc.
2. **Data extraction**: Unzips and loads raw ECG data from MIT-BIH AFDB.
3. **Preprocessing**: Bandpass filtering, segmentation, normalization.
4. **Patient-aware splitting**: Stratified train/test split to avoid data leakage.
5. **Feature extraction**: Time-domain & frequency-domain features (HRV, power).
6. **Modeling**:
  - Random Forest (classical ML)
  - 1D CNN (deep learning)
7. **Evaluation**: Classification report, confusion matrix, ROC AUC, learning curves.

---

## 📊 Key Features
- **Patient-aware split**: Ensures no patient appears in both train and test sets.
- **Stratification**: Maintains class balance for AF/Non-AF in both sets.
- **Feature engineering**: HRV metrics, spectral power, etc.
- **Model comparison**: Random Forest vs. 1D CNN.
- **Visualization**: EDA, class balance, confusion matrices, learning curves.

---

## 📝 How to Run
1. Clone this repo and open <span style="background:#e0e7ef; color:#1a237e; padding:2px 8px; border-radius:8px; font-weight:bold;">427_Project (3).ipynb</span> in Jupyter or VS Code.
2. Ensure you have Python 3.8+ and the required packages (see notebook for `pip install` commands).
3. Download the MIT-BIH AFDB ZIP and place it in the project folder.
4. Run all cells in order for full preprocessing, training, and evaluation.

---

## 📦 Dependencies
- `numpy`, `pandas`, `matplotlib`, `scikit-learn`, `wfdb`, `tqdm`, `tensorflow`, `scipy`

---

## 📈 Example Results
- <span style="background:#f1f8e9; color:#33691e; padding:2px 8px; border-radius:8px; font-weight:bold;">Random Forest</span>: Segment-level AF detection with ROC AUC and confusion matrix.
- <span style="background:#fce4ec; color:#ad1457; padding:2px 8px; border-radius:8px; font-weight:bold;">1D CNN</span>: End-to-end learning from raw ECG segments, with learning curves and evaluation metrics.

---

## 📄 References
- [MIT-BIH Atrial Fibrillation Database](https://physionet.org/content/afdb/1.0.0/)
- [WFDB Python Library](https://github.com/MIT-LCP/wfdb-python)

---

<div align="center">
  <b>CSE427 Project</b>
</div>
