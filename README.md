# task-7
# SVM Classification on Breast Cancer Dataset

## Objective
The goal of this project is to apply **Support Vector Machines (SVMs)** for both linear and non-linear classification on the Breast Cancer dataset.

## Tools Used
- **Python**
- **Scikit-learn**
- **NumPy**
- **Matplotlib**

---

## Steps Followed

### 1. Load and Prepare Dataset
- The dataset contains tumor features.
- Target variable: `diagnosis` (M = Malignant, B = Benign).
- We dropped the `id` column (not useful).
- Encoded target labels (M=1, B=0).
- Standardized features using `StandardScaler`.

### 2. Train SVM Models
- **Linear SVM**: Used kernel = 'linear'.
- **Non-linear SVM (RBF)**: Used kernel = 'rbf' with parameters C and gamma.

### 3. Visualization of Decision Boundary
- Used only 2 features (`radius_mean`, `texture_mean`) for visualization.
- Plotted decision boundaries for Linear and RBF kernels.

### 4. Hyperparameter Tuning
- Used **GridSearchCV** to find the best values of C and gamma.
- Best params: `C=1`, `gamma=0.01`.

### 5. Cross-validation Performance
- Linear SVM CV Score: ~0.965
- RBF SVM CV Score: ~0.970

---

## Results
- Both models perform well, but **RBF kernel slightly outperforms linear**.
- Decision boundaries show that RBF handles non-linear separation better.
