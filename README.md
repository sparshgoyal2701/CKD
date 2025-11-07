# Kidney Disease Prediction

A machine learning model that predicts chronic kidney disease using patient medical data.

## 📋 About

This project uses Random Forest classification to predict chronic kidney disease based on clinical parameters. The model processes 18 key medical features to provide accurate predictions.

## 🚀 Features

- Data preprocessing & cleaning
- Feature selection and engineering
- Random Forest classifier
- Model serialization with pickle
- 100% accuracy on test data

## 🛠️ Installation

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

## 💻 Usage

```python
import pickle
import pandas as pd

# Load model
model = pickle.load(open('kidney.pkl', 'rb'))

# Make prediction
sample_data = {
    'age': [48.0], 'bp': [70.0], 'al': [4.0], 'su': [0.0],
    'rbc': [0], 'pc': [1], 'pcc': [1], 'ba': [0],
    'bgr': [117.0], 'bu': [56.0], 'sc': [3.8], 'pot': [4.6],
    'wc': [6700], 'htn': [1], 'dm': [0], 'cad': [0],
    'pe': [1], 'ane': [1]
}

sample_df = pd.DataFrame(sample_data)
prediction = model.predict(sample_df)
print("CKD" if prediction[0] == 1 else "No CKD")
```

## 📊 Model Features

- **Demographic**: age, bp
- **Urine Tests**: al, su
- **Blood Tests**: bgr, bu, sc, pot, wc
- **Medical History**: htn, dm, cad
- **Symptoms**: rbc, pc, pcc, ba, pe, ane

## 📁 Files

- `kidney_disease.csv` - Dataset
- `kidney.pkl` - Trained model
- `kidney_prediction.ipynb` - Main code

## ⚠️ Note

Perfect accuracy may indicate overfitting. For medical use, consult healthcare professionals and validate with larger datasets.

## 📄 License

Educational use only.
```

This shorter version keeps all the essential information while being much more concise and easier to read quickly!
