# Framingham Heart Disease Prediction using Machine Learning

## Project Overview

This project uses machine learning classification algorithms to predict the **10-year risk of coronary heart disease (CHD)** using the Framingham Heart Disease dataset.

The target variable is **`TenYearCHD`**, where:
- `0` = No 10-year CHD risk indicated
- `1` = 10-year CHD risk indicated

The Jupyter Notebook performs data loading, inspection, exploratory data analysis, preprocessing, model training, prediction, and comparison of multiple classification algorithms.

## Dataset

The notebook uses the `framingham.csv` dataset.

The dataset contains **4,238 records and 16 columns**.

### Features

| Feature | Description |
|---|---|
| `male` | Gender indicator |
| `age` | Age of the individual |
| `education` | Education level |
| `currentSmoker` | Current smoking status |
| `cigsPerDay` | Cigarettes smoked per day |
| `BPMeds` | Blood pressure medication indicator |
| `prevalentStroke` | Previous stroke indicator |
| `prevalentHyp` | Hypertension indicator |
| `diabetes` | Diabetes indicator |
| `totChol` | Total cholesterol |
| `sysBP` | Systolic blood pressure |
| `diaBP` | Diastolic blood pressure |
| `BMI` | Body Mass Index |
| `heartRate` | Heart rate |
| `glucose` | Glucose level |
| `TenYearCHD` | Target: 10-year CHD outcome |

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Machine Learning Models

The notebook trains and evaluates the following classification models:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier
4. Support Vector Machine (SVM)
5. K-Nearest Neighbors (KNN)
6. Neural Network (MLP)

## Project Workflow

### 1. Import Libraries

Required Python libraries are imported for:
- Data manipulation
- Data visualization
- Data preprocessing
- Machine learning
- Model evaluation

### 2. Load Dataset

The Framingham dataset is loaded into a Pandas DataFrame.

```python
heart_data = pd.read_csv("framingham.csv")
```

> Update the file path if `framingham.csv` is stored in a different location.

### 3. Data Inspection

The notebook examines the dataset using operations such as:

- `head()`
- `tail()`
- `shape`
- `columns`
- `info()`
- `describe()`
- Missing-value checks
- Duplicate checks
- Target value counts

### 4. Exploratory Data Analysis

The notebook uses visualizations to understand the data, including:

- Count plots
- Histograms
- Box plots
- Correlation heatmap
- Distribution plots
- Pair plots where applicable

These visualizations help identify distributions, relationships, possible outliers, and correlations among variables.

### 5. Data Preprocessing

The preprocessing stage includes:

- Handling missing values using the median
- Removing duplicate records
- Separating features (`X`) and target (`y`)
- Splitting the data into training and testing sets
- Standardizing features using `StandardScaler`

The notebook uses an **80% training / 20% testing split**, with `random_state=42` and stratification.

### 6. Model Training

Each classification algorithm is trained using the processed training data and then used to make predictions on the test data.

### 7. Model Evaluation

The notebook evaluates models using:

- Accuracy
- Confusion Matrix
- Classification Report

## Model Performance

The final accuracy comparison obtained in the notebook is:

| Rank | Model | Accuracy |
|---:|---|---:|
| 1 | Support Vector Machine | 85.02% |
| 2 | Logistic Regression | 84.79% |
| 3 | Random Forest | 84.32% |
| 4 | K-Nearest Neighbors | 83.14% |
| 5 | Neural Network (MLP) | 81.49% |
| 6 | Decision Tree | 74.06% |

According to the notebook results, **Support Vector Machine (SVM)** achieved the highest accuracy of approximately **85.02%** among the evaluated models.

## Project Structure

```text
Framingham-Heart-Disease-Prediction/
│
├── 1feb4be9-ad62-4a0f-b24a-915665c139bc.ipynb
├── framingham.csv
└── README.md
```

## Requirements

Install the required Python packages using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

## How to Run

1. Install Python and the required libraries.
2. Place `framingham.csv` in the project directory.
3. Open Jupyter Notebook:

```bash
jupyter notebook
```

4. Open the `.ipynb` file.
5. Run the notebook cells from top to bottom.

## Results

The project demonstrates that machine learning classification algorithms can be applied to the Framingham dataset to classify the `TenYearCHD` outcome.

Among the models tested in this notebook, **SVM produced the best accuracy (85.02%)**, followed by Logistic Regression and Random Forest.

## Limitations

- Accuracy alone does not fully describe the performance of a medical-risk classification model.
- The project is based on the available Framingham dataset and its recorded variables.
- The model should not be considered a medical diagnostic system.
- Additional validation and clinically relevant evaluation would be required for real-world medical use.

## Conclusion

This project provides an end-to-end machine learning classification workflow for predicting the `TenYearCHD` outcome. It covers data inspection, exploratory analysis, preprocessing, feature scaling, classification, and model evaluation.

The comparison of six machine learning algorithms shows that the **Support Vector Machine achieved the highest test accuracy of approximately 85.02%** in the notebook.

## Author

Tadi Anu

---
