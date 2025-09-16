# HandigitsRecogntion-using-CNNcovenets

# Sign Language Digits Recognition using CNN  

This project implements a **Deep Convolutional Neural Network (CNN)** to classify digits (0–9) from hand gesture images in the **Sign Language Digits Dataset**.  
The work explores **hyperparameter tuning, regularization strategies, and model evaluation metrics** to study their impact on classification performance.  

---

## 📂 Dataset  
- Source: [Sign Language Digits Dataset](https://github.com/ardamavi/Sign-Language-Digits-Dataset)  
- Format: Images organized into 10 folders (0–9)  
- Total Samples: 2062 images  
- Split: **80% training (1650 images)**, **20% validation (412 images)**  
- Preprocessing: Images resized to `64x64` and normalized to `[0,1]`  

---

## 🧠 CNN Model Architecture  
- **Conv2D → MaxPooling → Conv2D → MaxPooling → Conv2D**  
- **Flatten → Dropout → Dense → Dense(softmax)**  
- Regularization options: L1, L2, L1+L2, Dropout, Early Stopping  
- Optimizer: Adam  
- Loss: Sparse Categorical Crossentropy  
- Output: 10-class softmax  

---

## ⚙️ Hyperparameters Explored  
1. **Batch Size**: 16, 32, 64, 128  
2. **Learning Rate**: 0.01, 0.001, 0.0001  
3. **Epochs**: 20, 30, 50+  
4. **Dropout Ratio**: 0.2, 0.5, 0.7  
5. **Early Stopping Patience**: 3, 5, 10  
6. **L1/L2 Regularization (λ)**: 0.0001, 0.001, 0.01  
7. **Normalization**: Pixel scaling to `[0,1]`  

---

## 📊 Evaluation Metrics  
- **Accuracy**  
- **Confusion Matrix**  
- **Precision, Recall, F1-score**  
- **AUC-ROC (One-vs-Rest)**  

Plots included:  
- Training vs. Validation Accuracy  
- Training vs. Validation Loss  
- Confusion Matrix Heatmap  

---

## 🚀 How to Run  
1. Clone the dataset:  
   ```bash
   git clone https://github.com/ardamavi/Sign-Language-Digits-Dataset.git
