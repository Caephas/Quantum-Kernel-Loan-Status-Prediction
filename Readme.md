# Quantum vs. Classical SVM Classification on Loan Dataset

This project demonstrates the use of Quantum Kernel methods to enhance the performance of Support Vector Machine (SVM) classifiers. We compare the performance of a Quantum Kernel-enhanced SVM with a classical SVM using a loan dataset.

## Project Overview

### Steps Involved

1. **Loading and Preparing the Data**:
   - The dataset `Loan_data.csv` was loaded, and features were separated from the target variable `Loan_Status`.

2. **Train-Test Split**:
   - The data was split into training and testing sets using an 80-20 split.

3. **Defining the Quantum Feature Map**:
   - A `ZZFeatureMap` was defined with 2 repetitions and linear entanglement to transform the classical data into a quantum feature space.

4. **Batch Processing for Kernel Evaluation**:
   - Due to the high memory requirements of evaluating the quantum kernel matrices, batch processing was implemented. This approach allowed the kernel matrices to be computed in smaller, manageable chunks to avoid memory overload.

5. **Training and Evaluating Quantum Kernel SVM**:
   - An SVM with a precomputed kernel was trained using the quantum kernel matrices.
   - The model was evaluated on the test set, and cross-validation was performed to ensure the robustness of the results.

6. **Training and Evaluating Classical SVM**:
   - A traditional SVM was trained using the raw features.
   - The model was evaluated on the test set, and cross-validation was performed to ensure the robustness of the results.

### Results

- **Quantum Kernel SVM**:
  - Classification accuracy: 78.90%
  - Cross-Validation Scores: [0.7471, 0.7586, 0.7011, 0.7701, 0.7126]
  - Mean CV Accuracy: 73.79%

- **Classical SVM**:
  - Classification accuracy: 67.89%
  - Cross-Validation Scores: [0.6782, 0.7011, 0.6897, 0.7471, 0.6897]
  - Mean CV Accuracy: 70.11%

### Conclusion

The results demonstrate that the Quantum Kernel-enhanced SVM outperforms the classical SVM in both direct accuracy and cross-validation metrics. This indicates the potential benefits of integrating quantum computing techniques into machine learning workflows.

### Batch Processing

Batch processing was crucial in this project to handle the large memory requirements of evaluating quantum kernel matrices. By processing the data in smaller chunks, we managed to avoid memory overload and efficiently compute the required matrices.
