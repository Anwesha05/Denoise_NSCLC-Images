# Denoise_NSCLC-Images
A Study of Denoising Techniques for Improved NSCLC  Classification Using WSI Histopathology Images.


## 📌 Overview

This project presents a comparative study of denoising techniques to improve classification accuracy of Non-Small Cell Lung Carcinoma (NSCLC) using Whole Slide Imaging (WSI) histopathology images. The goal is to enhance image quality through classical filtering methods and then classify subtypes of lung cancer using a deep learning-based CNN model.

---

## 👥 Team Members

- **Anwesha Pramanik** – BWU/MCA/23/043  
- **Avik Kumar Maiti** – BWU/MCA/23/010  
- **Subrata Dolui** – BWU/MCA/23/025  
- **Purajit Bera** – BWU/MCA/23/011  


---

## 🎯 Objectives

- 📂 Collect annotated WSI histopathological image tiles
- 🧽 Apply Bilateral, Gaussian, Median, and Wiener filters for denoising
- 🧠 Train a CNN model to classify lung cancer subtypes
- 📊 Evaluate performance using SNR, SSIM, Accuracy, Precision, Recall, F1-score
- 🏆 Identify the most effective denoising technique for pathology workflows

---

## 🧰 Tech Stack

- **Language:** Python  
- **Frameworks/Libraries:** TensorFlow, Keras, NumPy, OpenCV, Matplotlib, Scikit-learn  
- **Tools:** Jupyter Notebook, Anaconda, ImageScope  
- **Platform:** Local (Jupyter), GitHub

---

## 🗃️ Dataset

- **Total Images:** 11,580 histopathology tiles (size: 512×512 pixels)
- **Classes:**
  - Lung Adenocarcinoma (LUAD)
  - Lung Squamous Cell Carcinoma (LSCC)
  - Non-Malignant (NM)
- **Source:** 
  - ICMR-funded project (Apollo Hospitals)
  - The Cancer Imaging Archive (TCIA)
- **Format:** `.png` / `.tif` patches extracted from Whole Slide Images (WSI)
- **Split Ratio:** 
  - 80% Training  
  - 10% Validation  
  - 10% Testing

---

## ⚙️ Methodology

1. **Patch Extraction:**  
   Tiles were extracted from WSI using ImageScope and custom preprocessing tools.
2. **Noise Injection:**  
   Simulated image degradation using Gaussian, Speckle, and Salt & Pepper noise.
3. **Denoising Techniques Applied:**
   - Bilateral Filter
   - Gaussian Filter
   - Median Filter
   - Wiener Filter
4. **Model Architecture:**  
   A custom CNN with:
   - 6 Convolutional Layers  
   - 3 Max Pooling Layers  
   - Batch Normalization  
   - Fully Connected Dense Layer  
   - Dropout  
   - Softmax output for multi-class classification
5. **Evaluation Metrics:**
   - Accuracy
   - Precision
   - Recall
   - F1-Score
   - Structural Similarity Index (SSIM)
   - Signal-to-Noise Ratio (SNR)
   - Confusion Matrix

---

## 📈 Result Summary

| Filter Type | Accuracy | Precision | Recall | F1-Score | Notes |
|-------------|----------|-----------|--------|----------|-------|
| **Median**  | 99%      | 0.99      | 0.98   | 0.98     | Best performance across all metrics |
| Gaussian    | 98–99%   | 0.98      | 0.98   | 0.98     | Performs well, slight over-smoothing |
| Wiener      | 98%      | 0.98      | 0.97   | 0.97     | Adaptive filter with stable results |
| Bilateral   | 98%      | 0.97–0.98 | 0.97   | 0.97     | Preserves edges, converges faster |

✅ *The Non-Malignant class achieved 100% Precision, Recall, and F1-Score across all filter configurations.*

---

## 🚀 Future Scope

- Introduce **deep learning-based denoisers** like:
  - DnCNN  
  - Autoencoders  
  - GANs (e.g. Noise2Noise, Noise2Void)
- Apply **real-time deployment** strategies in clinical pathology labs
- Create a **web-based tool** to upload WSI and get live predictions
- Extend the model to handle **multi-organ cancer classification**
- Perform **cross-validation on diverse datasets** for generalization

---

## 📖 References

- 📄 **Dataset Source:** [The Cancer Imaging Archive (TCIA)](https://www.cancerimagingarchive.net/)
- 🧪 **ICMR-funded Research:** Apollo Hospitals' digital pathology project
- 📚 **Related Works & Algorithms:**
  - Papers and methods reviewed in the thesis report
  - SSIM, SNR calculation techniques
  - Custom CNN design patterns

---

## 🔗 Repository

👉 [GitHub Repository Link](https://github.com/Anwesha05/Denoise_NSCLC-Images)

---

## 🏷 License

> **Note:** This repository is part of an academic research project submitted for the MCA final year thesis at Brainware University.  


---

## 💬 Contact

- **Anwesha Pramanik**  
  GitHub: [Anwesha05](https://github.com/Anwesha05)  
  
- **Project Guide:**  
  Dr. Subrata Sinha  
  Professor, Department of Computational Sciences  
  Brainware University.
