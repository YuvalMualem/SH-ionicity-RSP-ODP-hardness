# Data-Driven Discovery of Self-Healing Mechanisms in Materials

This repository contains the data, analysis code, and machine learning workflow used in the study:

**"Possible Bond Character Effect on Self-Healing Properties of Materials for Sustainable Energy Conversion"**  
Yuval Mualem, David Cahen, Yevgeny Rakita, Hannah-Noa Barad (2025)
![Uploading ToC.png…]()

---

## Overview
The project explores how **bond-character descriptors** govern the **self-healing (SH)** behavior of materials relevant to energy generation and storage. The four bond parameters are:
1. **Ionicity:** defined by Linus Pauling as a function of the difference in electronegativities.
2. **RSP (Relative Structural Polarization):** the ratio of the ionic and electronic components of the dielectric function.
3. **ODP (Optical Deformation Potential):** the change in band gap under applied strain.
4. **Hardness:** the resistance to plastic deformation. 

By combining **data mining**, **feature correlation**, and **machine learning classification (SVM, Gaussian Mixture)**, we identify two main SH mechanisms:
1. **Class I “static lattice”:** via kinetically stabilized defects
2. **Class II “dynamic lattice”:** via thermodynamically stabilized defects

The workflow enables prediction of SH classes for new compounds based on their computed or measured properties.

---

## Workflow
1. **Data Analysis:**  
   The full dataset, found in table S1 (see `/Data/Supporting_Tables.xlsx`), is analyzed according to data type (computed / measured), materials groups and features.
   This is found in `Data Analysis.ipynb` (Figures 2, 3, 5 and Table 1 in main text).

2. **Classification Machine Learning (ML) Models:**
   Two classification models were trained on RSP-ODP map to classify between class I and class II:
   - **Support Vector Machine (SVM):** supervised learning
   - **Gaussian Mixture:** unsupervised learning
   Those models are used to classify new materials.
