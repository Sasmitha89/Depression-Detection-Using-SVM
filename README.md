# Depression Detection using Support Vector Machine (SVM)

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-success)
![University Project](https://img.shields.io/badge/University-AI%2FML-blueviolet)

---

## Project Overview

This project presents a machine learning approach for detecting depression using the **Support Vector Machine (SVM)** algorithm.

The model is trained on a balanced dataset and predicts whether an individual is likely to experience depression based on the given features.

This project was developed as part of the **Artificial Intelligence / Machine Learning** module at university.

---

## Objectives

- Build a binary classification model
- Perform dataset preprocessing
- Train an SVM classifier
- Evaluate model performance
- Compare different SVM kernels
- Save the trained model for future predictions

---

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib

---

## Project Structure

```
Depression-Detection-Using-SVM
│
├── data/
│   └── train_balanced.csv
│
├── notebooks/
│   └── SVM.ipynb
│
├── images/
│
├── svm_depression_model.pkl
│
├── requirements.txt
│
└── README.md
```

---

## Machine Learning Workflow

### 1. Import Required Libraries

The project uses Pandas, NumPy, Matplotlib, Seaborn and Scikit-learn.

---

### 2. Load Dataset

The depression dataset is loaded using Pandas.

```python
df = pd.read_csv("train_balanced.csv")
```

---

### 3. Exploratory Data Analysis

The notebook displays:

- Dataset shape
- First few records
- Dataset information
- Target distribution

---

### 4. Data Preparation

Features and target variable are separated.

```python
X = df.drop("Depression", axis=1)
y = df["Depression"]
```

---

### 5. Train-Test Split

The dataset is divided into:

- 80% Training
- 20% Testing

using stratified sampling.

---

### 6. Model Training

Support Vector Machine (SVM)

Kernel:

- RBF Kernel

```python
SVC(kernel="rbf")
```

---

### 7. Model Evaluation

The model is evaluated using

- Accuracy
- Classification Report
- Confusion Matrix

---

### 8. Cross Validation

5-Fold Cross Validation is used to measure model robustness.

---

### 9. Kernel Comparison

The following kernels are compared:

- Linear
- RBF
- Polynomial
- Sigmoid

---

### 10. Model Saving

The trained model is exported using Joblib.

```
svm_depression_model.pkl
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Depression-Detection-Using-SVM.git
```

Move into the project

```bash
cd Depression-Detection-Using-SVM
```

Install dependencies

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook

```bash
jupyter notebook
```

Open

```
SVM.ipynb
```

Run all cells.

---

## Results

The notebook evaluates the model using

- Accuracy Score
- Classification Report
- Confusion Matrix
- Cross Validation Accuracy
- Kernel Performance Comparison

SVM with linear kernel - Accuracy: 0.8398
SVM with rbf kernel - Accuracy: 0.8400
SVM with poly kernel - Accuracy: 0.8339
SVM with sigmoid kernel - Accuracy: 0.7754

## Future Improvements

- Hyperparameter tuning using GridSearchCV
- Feature selection
- ROC Curve analysis
- Precision-Recall analysis
- Web application using Flask or Streamlit
- Deep Learning comparison

---

## Author

Sasmitha Jayawardhana

BSc (Hons) Computer Systems and Network Engineering

Sri Lanka Institute of Information Technology (SLIIT)

---

## License

This project was developed for educational purposes as part of the Artificial Intelligence / Machine Learning module.
