# **Classification of Mobile Adware Variants Using Machine Learning Techniques**

## **Overview**  
Mobile adware is a major cybersecurity threat, affecting user privacy and device performance. This project classifies mobile adware variants using the **CIC-AndMal2017 dataset** and applies machine learning models:  
- **Logistic Regression** (baseline)  
- **Random Forest**  
- **XGBoost**  

Our results show that **XGBoost** outperforms other models with near-perfect accuracy (99%), precision, and recall, making it a robust tool for identifying adware variants.  

---

## **Dataset**  
The project uses the **CIC-AndMal2017 dataset** ([link](https://www.unb.ca/cic/datasets/andmal2017.html)), which contains:  
- Over **10,000 Android malware samples** categorized into **10 adware families** (e.g., Koodous, Gooligan, Feiwo).  
- Features include **network traffic statistics** like Flow Duration, Forward Packets/s, and Inter-Arrival Time (IAT).  

---

## **Methodology**  
### **Data Preprocessing**  
- **Handling Missing Data**: Removed columns with null or zero values.  
- **Normalization**: Scaled features using Min-Max scaling for uniformity.  
- **Feature Selection**: Used Information Gain to identify critical features like Flow Duration and Forward Packets/s.  
- **Data Splitting**: 80% training, 20% testing.  

### **Models Used**  
1. **Logistic Regression**: Baseline for comparison.  
2. **Random Forest**: Ensemble model for handling high-dimensional data.  
3. **XGBoost**: Gradient boosting model with regularization and parallel processing for optimal performance.  

---

## **Results**  
| **Model**           | **Accuracy (%)** | **Precision (%)** | **Recall (%)** | **F1-Score (%)** |  
|---------------------|------------------|-------------------|----------------|------------------|  
| Logistic Regression | 58               | 54                | 58             | 58               |  
| Random Forest       | 98               | 98                | 98             | 98               |  
| **XGBoost**         | **99**           | **99**            | **99**         | **99**           |  

### **Key Insights**  
- **XGBoost** outperforms others due to its gradient boosting mechanism and ability to handle imbalanced datasets.  
- Random Forest is effective but slightly less accurate than XGBoost.  
- Logistic Regression struggles with the complexity of adware data.  

---

## **Project Structure**  
