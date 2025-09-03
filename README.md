# MIT-BIH Atrial Fibrillation Detection Project

<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/2/2e/Electrocardiogram.png" alt="ECG Example" width="400"/>
  <br><br>
  <img src="https://raw.githubusercontent.com/mitdbg/ecg-figures/main/afib_example.png" alt="AFib Example" width="400"/>
</div>

<div align="center" style="margin: 20px 0;">
  <img src="https://img.shields.io/badge/Notebook-.ipynb-blue?style=for-the-badge&logo=jupyter"/>
  <img src="https://img.shields.io/badge/Deep%20Learning-1D%20CNN-orange?style=for-the-badge&logo=tensorflow"/>
  <img src="https://img.shields.io/badge/ML-Random%20Forest-green?style=for-the-badge&logo=scikit-learn"/>
  <img src="https://img.shields.io/badge/Data-MIT--BIH%20AFDB-purple?style=for-the-badge&logo=databricks"/>
</div>

---

## 📚 Overview
This project analyzes the MIT-BIH Atrial Fibrillation Database to detect atrial fibrillation (AF) from ECG signals using both classical machine learning and deep learning (1D CNN) approaches. All code and analysis are in the Jupyter notebook <span style="background:#e0e7ef; color:#1a237e; padding:2px 8px; border-radius:8px; font-weight:bold;">427_Project (3).ipynb</span>.

---

## 🖼️ ECG Signal Examples
<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/2/2e/Electrocardiogram.png" alt="Normal ECG" width="350" style="margin:10px; border-radius:12px; box-shadow:0 2px 8px #bdbdbd;"/>
  <img src="https://raw.githubusercontent.com/mitdbg/ecg-figures/main/afib_example.png" alt="Atrial Fibrillation ECG" width="350" style="margin:10px; border-radius:12px; box-shadow:0 2px 8px #bdbdbd;"/>
  <br>
  <span style="display:inline-block; background:#e3f2fd; color:#1565c0; padding:4px 12px; border-radius:16px; font-weight:bold; margin:8px;">Normal ECG</span>
  <span style="display:inline-block; background:#ffebee; color:#b71c1c; padding:4px 12px; border-radius:16px; font-weight:bold; margin:8px;">Atrial Fibrillation</span>
</div>

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
<span style="background:#e8f5e9; color:#1b5e20; padding:2px 8px; border-radius:8px; font-weight:bold;">1. Install dependencies</span>: `scikit-learn`, `wfdb`, `tqdm`, `tensorflow`, etc.<br>
<span style="background:#fffde7; color:#f9a825; padding:2px 8px; border-radius:8px; font-weight:bold;">2. Data extraction</span>: Unzips and loads raw ECG data from MIT-BIH AFDB.<br>
<span style="background:#e3f2fd; color:#1565c0; padding:2px 8px; border-radius:8px; font-weight:bold;">3. Preprocessing</span>: Bandpass filtering, segmentation, normalization.<br>
<span style="background:#fce4ec; color:#ad1457; padding:2px 8px; border-radius:8px; font-weight:bold;">4. Patient-aware splitting</span>: Stratified train/test split to avoid data leakage.<br>
<span style="background:#ede7f6; color:#4527a0; padding:2px 8px; border-radius:8px; font-weight:bold;">5. Feature extraction</span>: Time-domain & frequency-domain features (HRV, power).<br>
<span style="background:#f3e5f5; color:#6a1b9a; padding:2px 8px; border-radius:8px; font-weight:bold;">6. Modeling</span>:
   - Random Forest (classical ML)
   - 1D CNN (deep learning)
<span style="background:#e0f2f1; color:#00695c; padding:2px 8px; border-radius:8px; font-weight:bold;">7. Evaluation</span>: Classification report, confusion matrix, ROC AUC, learning curves.

---

## 📊 Key Features
- <span style="background:#f1f8e9; color:#33691e; padding:2px 8px; border-radius:8px; font-weight:bold;">Patient-aware split</span>: Ensures no patient appears in both train and test sets.
- <span style="background:#fff3e0; color:#e65100; padding:2px 8px; border-radius:8px; font-weight:bold;">Stratification</span>: Maintains class balance for AF/Non-AF in both sets.
- <span style="background:#e3f2fd; color:#1565c0; padding:2px 8px; border-radius:8px; font-weight:bold;">Feature engineering</span>: HRV metrics, spectral power, etc.
- <span style="background:#fce4ec; color:#ad1457; padding:2px 8px; border-radius:8px; font-weight:bold;">Model comparison</span>: Random Forest vs. 1D CNN.
- <span style="background:#ede7f6; color:#4527a0; padding:2px 8px; border-radius:8px; font-weight:bold;">Visualization</span>: EDA, class balance, confusion matrices, learning curves.

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
