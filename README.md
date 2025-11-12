# PercentileMethod_OL-Detection
# 📊 Detecting and Handling Outliers Using Percentile Method  
**AI Generated README**

---

## 📘 Overview
This project demonstrates **detecting and handling outliers using the Percentile Method**, an alternative to the IQR approach.  
We use a dataset containing **Gender**, **Height**, and **Weight** columns to identify and treat extreme values.

---

## ⚙️ Steps and Process

### **1. Dataset Overview**
- Dataset is available in the repository.  
- Features used: **Gender**, **Height**, and **Weight**.  
- **Box plot** was created to visualize the outliers.  
  🖼️ *<img width="562" height="396" alt="p1" src="https://github.com/user-attachments/assets/7b2dc1a6-bb7e-4c28-b6ac-717994b4f843" />
*

**Observation:**  
Outliers clearly visible in the height column — they need handling.  
Although IQR could be applied, this experiment focuses on the **Percentile Method**.

---

### **2. Data Distribution**
**Height Column Stats:**
- Mean = 66  
- Standard Deviation = 3.8  
- Min = 54  
- Max = 78  

**Distribution Plot:**
- Created using `distplot`.  
- Shows a roughly **normal distribution** of height values.  
  🖼️ <img width="576" height="432" alt="p2" src="https://github.com/user-attachments/assets/e408f5f1-9972-42fd-aa6f-df774d38e8c7" />


---

### **3. Defining Percentile Thresholds**
To detect outliers:
- **Upper Limit = 99th Percentile (Quantile 0.99)**  
- **Lower Limit = 1st Percentile (Quantile 0.01)**  

**Results:**
- Lower Limit = **58**  
- Upper Limit ≈ **74**

---
- After removal:
- **Mean** remained approximately the same.  
- **Max** reduced to 74.  
- **Min** increased to 58.

**Visualizations:**
- 🖼️ <img width="590" height="437" alt="p3" src="https://github.com/user-attachments/assets/2dba74b6-1620-4144-8383-232467b4f60b" />
 Distribution after trimming — similar shape, extremes removed.  
- 🖼️ <img width="576" height="394" alt="p4" src="https://github.com/user-attachments/assets/eabda58e-7f5d-4819-be05-b46c41d275a1" />
 Box plot after trimming — no visible outliers.

---

### **5. Handling Outliers (Capping / Winsorization)**
Instead of removing outliers, we can **cap** them:
- Replace values above the upper limit with the upper limit.  
- Replace values below the lower limit with the lower limit.

**Results:**
- Data at extremes slightly increased due to capping.  
- No outliers remained.

**Visualizations:**
- 🖼️ <img width="589" height="432" alt="p5" src="https://github.com/user-attachments/assets/113bd276-9319-4e03-ac49-3a8416096951" />
 Distribution after winsorization — small peaks at edges.  
- 🖼️ <img width="576" height="394" alt="p6" src="https://github.com/user-attachments/assets/4f35b105-0bff-4784-8b1b-81d81fa9a14d" />
 Box plot after winsorization — no outliers visible.

---


---

## 🧩 Key Insights
- The **Percentile Method** is useful when data roughly follows a **normal distribution**.  
- It is less influenced by extreme outliers compared to IQR.  
- **Trimming** removes outliers completely, maintaining a clean dataset.  
- **Winsorization (Capping)** preserves data size while reducing outlier impact.

---

> ⚠️ *This README is AI-generated and explains the process of detecting and handling outliers using the Percentile Method in an educational and experiment-style format.*

### **4. Removing Outliers (Trimming)**
- Created a new DataFrame containing only the records where:
