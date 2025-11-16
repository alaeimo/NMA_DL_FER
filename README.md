# A Transfer Learning Based Approach to Facial Emotion Recognition

A deep learning project utilizing transfer learning with pre-trained ResNet-18 to classify facial expressions into emotional categories using the FER2013 and CK+ datasets. This group effort from the Neuromatch Deep Learning Course (2023) explores improvements in facial emotion recognition (FER) for applications in security, marketing, and healthcare through fine-tuning, ensemble learning, and hyperparameter optimization. Pod Name: Bellusaurus_Line.

---

Example usage:
```bash
# Run the Jupyter notebook (no CLI flags; execute in Colab or locally)
jupyter notebook NMA_DL_FER.ipynb
# Or open in Google Colab for interactive execution
```

* No command-line flags are supported; all interactions are through the Jupyter notebook interface.
* Mount Google Drive to access datasets if needed.
* Run cells to train the model and visualize results.

---

## 🧩 Features

* 📅 Utilizes FER2013 and CK+ datasets with 48x48 grayscale images and emotional labels for training
* 🛡️ Applies data preprocessing including illumination normalization, random cropping, and horizontal flipping for augmentation
* 🤖 Implements transfer learning with ResNet-18, fine-tuning, and ensemble approaches to boost accuracy
* 🎯 Minimizes cross-entropy loss with adaptive learning rates, optimizers (Adam/SGD), and hyperparameter tuning
* ✉️ Evaluates model performance with accuracy metrics on train/validation/test sets and confusion matrices
* 🖥️ Visualizes results using Matplotlib for loss/accuracy plots and sample predictions
* ⚡ Explores limitations like image resolution and class imbalance for future improvements

---

## 🛠️ Tech Stack

| Category       | Technologies              |
| -------------- | ------------------------- |
| Programming    | Python                    |
| Deep Learning  | PyTorch, Torchvision      |
| Data Processing| Pandas, NumPy, Matplotlib |
| Model Summary  | Torchinfo                 |
| Progress       | TQDM                      |

---

## 🧠 How It Works

1. **Dataset Preparation**
   Load FER2013 and CK+ datasets, normalize images for illumination, and apply augmentations like random cropping and flipping to enhance variety.

2. **Model Setup**
   Use pre-trained ResNet-18, modify the final layer for 7 emotion classes (angry, disgust, fear, happy, neutral, sad, surprise), and apply transfer learning or fine-tuning.

3. **Training Process**
   Train the model by minimizing cross-entropy loss using optimizers like Adam or SGD, with adaptive learning rates (e.g., StepLR or CosineAnnealingLR) over multiple epochs.

4. **Ensemble Learning**
   Experiment with feature-level ensemble methods to combine predictions and improve overall accuracy.

5. **Evaluation**
   Assess performance on validation and test sets, generating confusion matrices to analyze misclassifications, and test on CK+ for cross-dataset validation.

---

## 🧾 Example

**Model Results Summary:**

| Method/Model | Train Acc(%) | Validation Acc(%) | Test Acc(%) | FER2013 Test Acc(%) | CK+ Acc(%) | Learning Rate | Optimizer | Batch Size | Epochs | Trainable Parameters |
|--------------|--------------|-------------------|-------------|---------------------|-------------|---------------|-----------|------------|--------|----------------------|
| ResNet18 Transfer Learning | 31.04 | 31.64 | 31.98 | - | - | Adaptive (StepLR) | Adam | 256 | 10 | 3.5K |
| S-ResNet18 | 87.13 | 65.86 | 67.26 | 67.58 | - | CosineAnnealingLR | Adam | 128 | 50 | 11M |
| Feature-Level Ensemble | 82.3 | 64.92 | 66.17 | 59.42 | - | CosineAnnealingLR | SGD | 64 | 20 | 132K |
| ResNet18 Fine Tuning | 86.86 | 69.29 | 70.10 | 68.70 | - | Adaptive (StepLR) | Adam | 128 | 20 | 11M |

**Confusion Matrix Analysis:**
The model shows higher accuracy for emotions like "happy" and "neutral" but lower for "disgust" due to class imbalance in the datasets.

---
## 🧾 **Report**

A detailed report describing the dataset, methodology, experimental setup, and findings is available in the repository:
📄 [Report (PDF)](./Report.pdf)

## 👨‍💻 About the Authors

**Group Members (Bellusaurus_Line Pod):**  
- Mohammad Alaei 🔗 [https://alaeimo.ir](https://alaeimo.ir)
- Rishabh Bapat (rishabhbapat@gmail.com)  
- Zahra Noori (zs.noori@gmail.com)   


This project showcases expertise in deep learning for computer vision, transfer learning techniques, and performance optimization in emotion recognition systems, contributing to advancements in AI-driven affective computing.
