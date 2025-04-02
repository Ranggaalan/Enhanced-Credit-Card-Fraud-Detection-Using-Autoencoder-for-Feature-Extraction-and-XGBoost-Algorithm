# **Credit Card Fraud Detection Using Autoencoder and XGBoost**  

📌 **Project Description**  
This project aims to detect **credit card fraud** using a **hybrid deep learning and machine learning approach**. The dataset, sourced from **Kaggle**, contains anonymized transaction data with **high-class imbalance** (fraud cases account for only 0.172% of transactions). To improve fraud detection, we apply **Autoencoder for feature extraction** and **XGBoost for classification**, leveraging their combined strengths in anomaly detection and ensemble learning.  
![image](https://github.com/user-attachments/assets/8de017c3-c8fd-4c61-ae0e-5166fd7d2616)


📝 **Dataset**  
**Source**: [Kaggle - Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)  
**Size**: 284,807 transactions (492 fraud cases)  

**Features**:  
- **V1 - V28** – Principal Component Analysis (PCA) transformed numerical features  
- **Time** – Seconds elapsed since the first transaction  
- **Amount** – Transaction amount  
- **Class** – Target variable (0 = Non-fraud, 1 = Fraud)  

🔍 **Methodology**  

📌 **Exploratory Data Analysis (EDA)**  
- Fraud vs. non-fraud transaction distribution  
- Correlation heatmap to analyze feature relationships  
- Boxplots to detect outliers in transaction amounts  

📌 **Data Preprocessing**  
- Handling class imbalance using **oversampling (ADASYN)**  
- Feature scaling using **MinMaxScaler**  
- Splitting dataset into **training (80%)** and **testing (20%)**  

📌 **Models Used**  
✔ **Autoencoder + XGBoost (Best Model: AUC-ROC = 0.977, Training Time: 2m 3s)**  
✔ **Standard XGBoost (AUC-ROC = 0.968, Training Time: 9s)**  
✔ **Standalone Autoencoder (AUC-ROC = 0.942, Training Time: 6m 20s)**  

📌 **Model Evaluation Metrics**  
- **AUC-ROC Score** (Key metric for imbalanced classification)  
- **Precision-Recall Curve**  
- **F1-Score**  
- **Training Time Analysis**  

📊 **Results**  

### EDA
![image](https://github.com/user-attachments/assets/d2d7f648-2bb5-49a0-807b-0eb2fe4e2308)

### Build Model 
![image](https://github.com/user-attachments/assets/ef59eb6f-e823-446f-9017-d50a4815d50d)

### Train Model
![image](https://github.com/user-attachments/assets/ed3bb34b-eca8-455b-a2e0-db7a43159c80)

📌 **Comparison of Models**  

![image](https://github.com/user-attachments/assets/6f0b6d78-b9ed-49c6-b04e-a1aba766d4c5)

| Model                   | AUC-ROC Score | Training Time  |  
|------------------------|-------------|--------------|  
| **Autoencoder + XGBoost** | **0.977**    | **2m 3s**      |  
| Standard XGBoost       | 0.968       | 9s           |  
| Standalone Autoencoder | 0.942       | 6m 20s       |  

📌 **Key Visualizations**  
- ROC Curve Comparison  
- Fraud Transaction Distribution  
- Feature Importance Analysis  

💻 **Technologies Used**  
- **Python**: Pandas, NumPy, Scikit-learn, TensorFlow, XGBoost, Matplotlib, Seaborn  
- **Deep Learning**: Autoencoder (Keras)  
- **Machine Learning**: XGBoost for classification  
- **Evaluation Metrics**: AUC-ROC, Precision-Recall Curve  

🔥 **Conclusion**  
The **Autoencoder + XGBoost model** achieved the **highest AUC-ROC score (0.977)**, outperforming standalone **XGBoost (0.968)** and **Autoencoder (0.942)**. This hybrid approach efficiently detects fraudulent transactions while maintaining a **reasonable training time (2m 3s)**. The results demonstrate that deep learning-based feature extraction combined with ensemble learning can significantly enhance fraud detection in imbalanced datasets.  
