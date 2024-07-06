# Breast Cancer Classification System


## Project Overview
This project aims to analyze the Breast Cancer Wisconsin (Diagnostic) dataset and build machine learning models to predict whether a breast cancer diagnosis is malignant or benign based on the physical characteristics of the tumor.

## Dataset Overview
The dataset contains information about breast cancer diagnoses, with 569 rows and 32 columns. Each row represents a patient, and the columns represent various physical characteristics of the tumors along with the diagnosis label (M = malignant, B = benign).

### Source
- **UW CS FTP Server**: ftp.cs.wisc.edu (path: `/math-prog/cpo-dataset/machine-learn/WDBC/`)
- **UCI Machine Learning Repository**: [Breast Cancer Wisconsin (Diagnostic) Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)

## Attribute Information
1. **ID number**
2. **Diagnosis**: (M = malignant, B = benign)
3. **Features (3-32)**: Ten real-valued features computed for each cell nucleus:
   - a) **Radius**: Mean of distances from center to points on the perimeter
   - b) **Texture**: Standard deviation of gray-scale values
   - c) **Perimeter**
   - d) **Area**
   - e) **Smoothness**: Local variation in radius lengths
   - f) **Compactness**: (perimeter^2 / area - 1.0)
   - g) **Concavity**: Severity of concave portions of the contour
   - h) **Concave points**: Number of concave portions of the contour
   - i) **Symmetry**
   - j) **Fractal dimension**: ("coastline approximation" - 1)
   
The mean, standard error, and "worst" or largest (mean of the three largest values) of these features were computed for each image, resulting in 30 features.

### Class Distribution
- **Benign**: 357
- **Malignant**: 212

### Missing Attribute Values
- None

## Project Workflow

### 1. Data Preprocessing
- **Handling Missing Values**: Dropped the empty `Unnamed: 32` column.
- **Data Normalization**: Normalized features to ensure a similar scale.
- **Feature Selection**: Selected features with high correlation to the target variable.

### Tools Used
- **Pandas**: Data manipulation and cleaning.
- **Scikit-learn**: Data normalization and feature selection.

### 2. Exploratory Data Analysis (EDA)
- **Visualizations**: Histograms, correlation heatmaps, and box plots to understand feature distributions and relationships.
- **Key Findings**: Significant differences between malignant and benign tumors in features such as `radius_mean`, `texture_mean`, `perimeter_mean`, `area_mean`, and `concavity_mean`.

### 3. Model Selection
- **Algorithms Used**: Logistic Regression, Support Vector Machine (SVM), Random Forest, K-Nearest Neighbors (KNN).
- **Evaluation Metrics**: Accuracy, precision, recall, and F1 score.

#### Performance Comparison
- **Random Forest**: Accuracy 96%, Precision 95%, Recall 96%, F1 Score 95%
- **SVM**: Accuracy 94%, Precision 93%, Recall 94%, F1 Score 93%

### 4. Results and Discussion
- **Best Model**: Random Forest with the highest overall performance.
- **Key Features**: `radius_mean`, `texture_mean`, and `perimeter_mean`.
- **Implications**: Potential for improving early breast cancer detection and diagnosis.

### 5. Future Research
- Hyperparameter tuning, incorporating additional features or datasets, and exploring deep learning models.

## Conclusion
- **Summary**: Machine learning models, especially Random Forest and SVM, can accurately predict breast cancer diagnoses based on tumor characteristics.
- **Impact**: These models can support medical professionals in early and accurate breast cancer diagnosis, enhancing clinical decision-making.

## References
- UCI Machine Learning Repository: [Breast Cancer Wisconsin (Diagnostic) Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)
- [K. P. Bennett and O. L. Mangasarian: "Robust Linear Programming Discrimination of Two Linearly Inseparable Sets", Optimization Methods and Software 1, 1992, 23-34]
