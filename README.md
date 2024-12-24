# AI-for-Cybersecurity

# CICIDS Friday Working Hours Afternoon DDoS Detection

## Project Overview

This project involves processing and building machine learning models to classify and detect Distributed Denial of Service (DDoS) attacks in network traffic data. The dataset used is from the **Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv** file, which contains various network features captured during a typical working day with simulated DDoS attacks. The goal of this project is to preprocess the dataset, train classification models, and compare the performance of different machine learning algorithms.

## Dataset Description

The dataset used in this project contains network traffic features related to both benign (normal) and malicious (DDoS) network behavior. Key features include:
- Flow Duration
- Total Forward and Backward Packets
- Packet Lengths (Max, Min, Mean, etc.)
- Flags indicating the state of TCP connections (e.g., SYN, ACK, URG)
- Data Transfer Rates
- Idle/Active Time Statistics
- Labels (Benign or Attack)

## Project Steps

The project involves the following steps:

### 1. **Dataset Loading & Initial Inspection**
   - The dataset is loaded into a pandas DataFrame.
   - Basic exploration is performed to inspect the shape and columns.

### 2. **Data Cleaning**
   - Missing or infinite values are replaced with `NaN`, and rows containing missing values are dropped.

### 3. **Feature Selection**
   - Irrelevant columns such as "Flow ID", "Source IP", "Destination IP", and "Timestamp" are dropped to focus on meaningful features.
   
### 4. **Label Encoding**
   - The target variable, `Label`, which represents whether the flow is benign or an attack, is encoded using `LabelEncoder` from `sklearn`.

### 5. **Feature Scaling**
   - Numerical features are standardized using `StandardScaler` to normalize their scale and improve the performance of the machine learning models.

### 6. **Feature Selection (Optional)**
   - The `SelectKBest` method with the `f_classif` score function is used to select the top 20 most relevant features based on statistical significance.

### 7. **Handling Class Imbalance**
   - The dataset is balanced using **SMOTE** (Synthetic Minority Over-sampling Technique) to handle class imbalance between benign and attack samples.

### 8. **Model Training**
   - **Support Vector Machine (SVM)** and **Decision Tree Classifier** models are trained on the preprocessed dataset.

### 9. **Model Evaluation**
   - Both models are evaluated on a test set, and their accuracy and classification reports are generated.
   - A comparison of the two models' accuracy is visualized using a bar chart.

### 10. **Model Comparison**
   - The accuracy scores of both models (SVM and Decision Tree) are compared to determine which model performs better on the dataset.

### 11. **Saving the Preprocessed Data**
   - The preprocessed dataset is saved as a CSV file for future use.

### 12. **Final Output**
  -The shapes of the training and testing sets, as well as the class distribution in the training set, are printed to provide insights into the final dataset.
   Dependencies

### Explanation:
- The description provides a brief overview of the dataset and what the project aims to achieve.
- Steps of the project are clearly outlined with explanations of data preprocessing and modeling.
- Usage instructions and installation requirements are included to ensure that others can run the project.
- A conclusion section summarizes the project and the models used.



