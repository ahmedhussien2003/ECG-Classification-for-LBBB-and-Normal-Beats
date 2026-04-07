# ECG Classification for LBBB and Normal Beats

An end-to-end machine learning pipeline for detecting **Left Bundle Branch Block (LBBB)** from **Electrocardiogram (ECG)** signals using signal preprocessing, wavelet-based feature extraction, and K-Nearest Neighbors (KNN) classification.

---

## 📌 Overview

Left Bundle Branch Block (LBBB) is a cardiac conduction abnormality characterized by prolonged QRS complexes in ECG signals. Manual ECG interpretation requires clinical expertise and can be time-consuming.  

This project provides an automated system that processes raw ECG signals, extracts meaningful features, and classifies heartbeats into:

- ✅ **Normal Beats**
- ❤️ **LBBB Beats**

The pipeline combines **signal processing** and **machine learning** to create a reliable ECG classification workflow.

---

## ⚙️ Pipeline Architecture

The system follows these main stages:

1. **ECG Preprocessing**
2. **QRS Detection & Beat Segmentation**
3. **Wavelet Feature Extraction**
4. **Machine Learning Classification**
5. **Automated Prediction**

---

## 🔧 Preprocessing

ECG signals are cleaned and enhanced using:

- Butterworth **Bandpass Filter** (removes noise)
- **Baseline Wander Removal**
- Savitzky–Golay **Noise Reduction**
- **QRS Complex Detection** for heartbeat localization

These steps preserve important ECG components (P, QRS, T waves).

---

## 📊 Feature Extraction

Features are extracted using the **Discrete Wavelet Transform (DWT)**:

- Wavelet type: `db3` (Daubechies)
- Multi-level decomposition
- Captures both time and frequency characteristics
- Effective for detecting QRS morphology variations in LBBB

---

## 🤖 Classification

The project uses **K-Nearest Neighbors (KNN)** for classification.

**Why KNN?**
- Simple and interpretable
- Effective for biomedical datasets
- Works well with wavelet feature space

Each beat is classified based on similarity to neighboring samples.

---

## 🔍 Prediction Workflow

The prediction pipeline:

1. Load ECG signal
2. Apply preprocessing filters
3. Detect QRS complexes
4. Segment heartbeats
5. Extract wavelet features
6. Predict beat labels
7. Apply majority voting for final classification

---

## 🧰 Tech Stack

- Python
- NumPy
- SciPy
- PyWavelets
- Scikit-learn
- Signal Processing Techniques

---

## 🚀 Use Cases

- ECG signal analysis
- Cardiac abnormality detection
- Biomedical signal processing research
- Machine learning in healthcare applications

---

## 📈 Possible Improvements

- Support Vector Machine (SVM) classifier
- Random Forest models
- Deep Learning (CNN-based ECG classification)
- Heart Rate Variability (HRV) features
- Adaptive noise filtering

---

## ✅ Conclusion

This project demonstrates a complete ECG classification pipeline combining signal preprocessing, wavelet feature extraction, and machine learning to distinguish between Normal and LBBB heartbeats. The system provides a strong foundation for automated cardiac diagnosis and future AI-based healthcare solutions.

---

## 📄 License

This project is open-source and available under the MIT License.
