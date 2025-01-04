# Cardiac Arrhythmia Detection  

## Introduction  
The Cardiac Arrhythmia Detection project utilizes a comprehensive dataset from the **UCI Machine Learning Repository** to classify and predict arrhythmias. This dataset serves as a valuable resource for developing machine learning models to detect various heart conditions and arrhythmic patterns.  

**Dataset Link:** [UCI Arrhythmia Dataset](https://archive.ics.uci.edu/ml/datasets/Arrhythmia)  

### Key Highlights:  
- **Total Instances:** 452  
- **Normal Cases:** 245  
- **Arrhythmia Types:** 12 distinct classes representing various heart conditions  
- **Features:** 279 attributes, including patient demographics, heart activity measurements, and waveform data  
- **Classification Goal:**  
  - Predict if a patient has an arrhythmia.  
  - If arrhythmia is present, classify the condition into one of the 12 available categories.  

---

## Dataset Overview  

### Number of Instances  
- **Total Samples:** 452  

### Number of Attributes  
- **Total Attributes:** 279  
- **Linear Attributes:** 206  
- **Nominal Attributes:** 73  

---

## Attribute Information  

### Demographic and Basic Clinical Data (1–5)  
- **Age:** Age in years (Linear)  
- **Sex:** 0 = Male; 1 = Female (Nominal)  
- **Height:** Height in centimeters (Linear)  
- **Weight:** Weight in kilograms (Linear)  
- **Heart Rate:** Number of heartbeats per minute (Linear)  

---

### Electrocardiogram (ECG) Measurements (6–15)  
- **QRS Duration:** Average duration of QRS complex (ms)  
- **P-R Interval:** Average time between P wave onset and Q wave onset (ms)  
- **Q-T Interval:** Average time from Q wave onset to T wave offset (ms)  
- **T Interval:** Average T wave duration (ms)  
- **P Interval:** Average P wave duration (ms)  

**Vector Angles (Degrees) on the Frontal Plane:**  
- **QRS**  
- **T**  
- **P**  
- **QRST**  
- **J**  

---

### Detailed Waveform Data (16–27) – Channel DI  
- **Q Wave Width (ms)**  
- **R Wave Width (ms)**  
- **S Wave Width (ms)**  
- **R’ Wave Width (ms)**  
- **S’ Wave Width (ms)**  
- **Number of Intrinsic Deflections (Linear)**  

**Nominal Attributes – ECG Morphology Indicators:**  
- **Ragged R Wave**  
- **Diphasic R Wave**  
- **Ragged P Wave**  
- **Diphasic P Wave**  
- **Ragged T Wave**  
- **Diphasic T Wave**  

---

### Additional ECG Channels  
**Channels Represented:**  
- **DII (28–39)**  
- **DIII (40–51)**  
- **AVR (52–63)**  
- **AVL (64–75)**  
- **AVF (76–87)**  
- **V1 to V6 (88–159)**  

**Amplitude Measurements (x0.1 mV):**  
- **JJ Wave**  
- **Q Wave**  
- **R Wave**  
- **S Wave**  
- **R’ Wave**  
- **S’ Wave**  
- **P Wave**  
- **T Wave**  

**Calculated Indices:**  
- **QRSA:** Sum of areas of all segments / 10  
- **QRSTA:** QRSA + 0.5 * T wave width * 0.1 * T wave height  

---

## Missing Values  
- **Missing Data:** Some attributes contain missing values, represented by `?`.  

---

## Class Distribution  

| Class Code | Condition                                   | Instances |  
|------------|---------------------------------------------|-----------|  
| 01         | Normal                                      | 245       |  
| 02         | Ischemic changes (Coronary Artery Disease)   | 44        |  
| 03         | Old Anterior Myocardial Infarction           | 15        |  
| 04         | Old Inferior Myocardial Infarction           | 15        |  
| 05         | Sinus Tachycardia                            | 13        |  
| 06         | Sinus Bradycardia                            | 25        |  
| 07         | Ventricular Premature Contraction (PVC)      | 3         |  
| 08         | Supraventricular Premature Contraction       | 2         |  
| 09         | Left Bundle Branch Block                     | 9         |  
| 10         | Right Bundle Branch Block                    | 50        |  
| 11         | 1st Degree AV Block                          | 0         |  
| 12         | 2nd Degree AV Block                          | 0         |  
| 13         | 3rd Degree AV Block                          | 0         |  
| 14         | Left Ventricular Hypertrophy                 | 4         |  
| 15         | Atrial Fibrillation or Flutter               | 5         |  
| 16         | Other Conditions                             | 22        |  

---

## Observations and Challenges  
- **Imbalance in Class Distribution:**  
  - The dataset is heavily skewed towards normal cases (245), with limited representation for certain arrhythmias like **Ventricular Premature Contraction (3 instances)** and **Supraventricular Premature Contraction (2 instances).**  
- **High Dimensionality:**  
  - The dataset contains 279 attributes but only 452 samples, which may lead to overfitting without proper dimensionality reduction or feature selection.  

---

## Project Goals and Objectives  
- **Primary Objective:**  
  - Predict the presence or absence of arrhythmia.  
- **Secondary Objective:**  
  - Classify arrhythmia cases into one of 12 specific types.  

By applying machine learning algorithms, this project aims to enhance the early detection and classification of heart conditions, contributing to improved healthcare diagnostics and patient outcomes.  
