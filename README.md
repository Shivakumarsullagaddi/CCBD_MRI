# CCBD_MRI

## 1. Problem Definition & Data Preparation

**Goal:** Detect and analyze hippocampal and cortical atrophy in MRI scans for Alzheimer’s disease research.

**Dataset:** Organized MRI NIfTI files by diagnostic class (`AD`, `CN`, `MCI`), with each subject having an MRI and metadata.

---

## 2. Initial Experiments: 2D Classification

- **Started with:** 2D CNNs on individual MRI slices.
- **Challenge:** 2D models failed to capture 3D anatomical context, leading to limited accuracy and poor generalization.

---

## 3. Transition to 3D Deep Learning

- **Moved to:** 3D ResNet and 3D CNNs, processing full MRI volumes.
- **Benefit:** Captured spatial relationships between slices, improving classification performance.
- **Problem:** Computational requirements increased; model training was slower and required more memory.








## 📘 Learnings

- **3D Images** require more computation (GPUs).  
  - 🧠 They **take significantly more time** when run on CPU.

- When the **Dataset is SMALL** and the model is **Overfitting**:  
  - ✅ Use **Data Augmentation**  
  - ✅ Apply **Regularization**

- When the model has **Poor Generalization**:  
  - 🔁 Use **Transfer Learning**

- When facing issues in **loading huge datasets** during training on GPU:  
  - ⚙️ Use **Mixed Precision Training**

- When all else is good (no issues):  
  - 🔧 Try tuning **Epochs**, **Batch Size**, **Learning Rate**, and observe performance.

