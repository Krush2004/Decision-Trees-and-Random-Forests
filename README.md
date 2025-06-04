# ❤️ Heart Disease Prediction with Decision Trees & Random Forests

This project uses tree-based machine learning models to predict the presence of heart disease using clinical features from the **Heart Disease Dataset**.

---

## 📁 Dataset

**File**: `heart.csv`  
**Rows**: 303  
**Columns**: 14 (13 features + 1 target)

### 🔸 Features

| Feature      | Description |
|--------------|-------------|
| `age`        | Age of the patient |
| `sex`        | 1 = male, 0 = female |
| `cp`         | Chest pain type (0–3) |
| `trestbps`   | Resting blood pressure (mm Hg) |
| `chol`       | Serum cholesterol (mg/dl) |
| `fbs`        | Fasting blood sugar > 120 mg/dl (1 = true; 0 = false) |
| `restecg`    | Resting ECG results (0–2) |
| `thalach`    | Max heart rate achieved |
| `exang`      | Exercise induced angina (1 = yes; 0 = no) |
| `oldpeak`    | ST depression |
| `slope`      | Slope of peak ST segment (0–2) |
| `ca`         | Number of major vessels (0–3) colored by fluoroscopy |
| `thal`       | Thalassemia (0 = normal, 1 = fixed defect, 2 = reversible defect) |
| `target`     | **Target**: 1 = disease, 0 = no disease |

---

## 🧰 Tools & Libraries

- Python 3.x
- `pandas`, `numpy`
- `matplotlib`
- `scikit-learn`

---

## 🚀 Model Pipeline

### ✅ Steps Performed

1. **Data Loading**: Loads `heart.csv` and checks for missing values.
2. **Train-Test Split**: Splits the data into 80% training and 20% testing.
3. **Decision Tree Classifier**:
   - Trained and visualized with `plot_tree()`.
   - Accuracy printed for both train and test sets.
4. **Overfitting Check**:
   - Decision Trees retrained with various `max_depth` values.
5. **Random Forest Classifier**:
   - Trained with 100 estimators.
   - Accuracy printed for both train and test sets.
6. **Feature Importance**:
   - Extracted from the trained Random Forest.
   - Bar plot visualized using `matplotlib`.
7. **Cross-Validation**:
   - 5-fold cross-validation scores computed for both models.

---

## 📊 Example Output

Decision Tree Train Accuracy: 1.0
Decision Tree Test Accuracy: 0.9853658536585366
****************
Overfitting Analysis:
Depth=2: Train Acc=0.77, Test Acc=0.68
Depth=4: Train Acc=0.88, Test Acc=0.80
Depth=6: Train Acc=0.95, Test Acc=0.88
Depth=8: Train Acc=0.99, Test Acc=0.98
Depth=10: Train Acc=1.00, Test Acc=0.99
****************
Feature Importances:
cp: 0.1351
ca: 0.1273
thalach: 0.1222
oldpeak: 0.1219
thal: 0.1105
age: 0.0779
chol: 0.0748
trestbps: 0.0712
exang: 0.0576
slope: 0.0458
sex: 0.0287
restecg: 0.0186
fbs: 0.0084
****************
Decision Tree CV Accuracy: 1.00
Random Forest CV Accuracy: 1.00

---

## 🏁 How to Run
1. Place `heart.csv` in the same folder as your `.py` file.
2. Install dependencies if needed:
   ```bash
   pip install pandas numpy matplotlib scikit-learn
   
