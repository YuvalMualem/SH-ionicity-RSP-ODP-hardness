# Data-Driven Discovery of Self-Healing Mechanisms in Materials

This repository contains the data, analysis code, and machine learning workflow used in the study:

**"Possible Bond Character Effect on Self-Healing Properties of Materials for Sustainable Energy Conversion"**  
Yuval Mualem, David Cahen, Yevgeny Rakita, Hannah-Noa Barad (2025)

---

## Overview
The project explores how **bond-character descriptors** govern the **self-healing (SH)** behavior of materials relevant to energy generation and storage. The four bond parameters are:
1. **Ionicity:** defined by Linus Pauling as a function of the difference in electronegativities.
2. **RSP (relative structural polarization):** the ratio of the ionic and electronic components of the dielectric function.
3. **ODP (optical deformation potential):** the change in band gap under applied strain.
4. **Hardness:** the resistance to plastic deformation. 

By combining **data mining**, **feature correlation**, and **machine learning classification (SVM, Gaussian Mixture Models)**, we identify two main SH mechanisms:
1. **Class I “static lattice”:** via kinetically stabilized defects
2. **Class II: “dynamic lattice”:** via thermodynamically stabilized defects

The workflow enables prediction of SH classes for new compounds based on their computed or measured properties.

---

## Workflow
2. **Feature Engineering:**  
   Clean, normalize, and combine data to generate the full dataset (`data/processed/`).

3. **Machine Learning:**  
   - Train SVM and Gaussian Mixture models for classification.  
   - Visualize decision boundaries (ODP–RSP map, Hardness–RSP map).

4. **Prediction:**  
   Apply models to predict the SH class of new materials.

---

## Data
Each dataset includes the following fields:
| Property | Unit |
|-----------|-------------|
| `ODP` | Optical Deformation Potential (eV) |
| `RSP` | Relative Structural Polarization |
| `ionicity` | Bond ionicity (0–1) |
| `hardness` | Vickers microhardness (GPa) |
