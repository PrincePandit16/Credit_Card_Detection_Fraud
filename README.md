# 💳 Credit Card Fraud Detection

A machine learning project to detect fraudulent credit card transactions using the [Kaggle Credit Card Fraud Detection dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).

---

## 📂 Dataset Setup (Required)

> ⚠️ The dataset is **not included** in this repository due to its size. You must download it manually from Kaggle.

### Step 1 — Download the Dataset

1. Go to the Kaggle dataset page:  
   👉 [https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

2. Click the **Download** button (you must be logged in to Kaggle).

3. Extract the downloaded zip file. You will get a file named `creditcard.csv`.

### Step 2 — Place the Dataset

Place `creditcard.csv` in the **root directory** of this project:

```
Credit_Card_Detection_Fraud/
├── creditcard.csv        ← Place the file here
├── main.py
├── new.ipynb
├── requirements.txt
└── README.md
```

### (Optional) Download via Kaggle API

If you have the [Kaggle CLI](https://github.com/Kaggle/kaggle-api) installed:

```bash
kaggle datasets download -d mlg-ulb/creditcardfraud
unzip creditcardfraud.zip
```

---

## 📊 About the Dataset

| Property       | Details                                     |
|----------------|---------------------------------------------|
| Source         | Kaggle / ULB Machine Learning Group         |
| Records        | 284,807 transactions                        |
| Fraud Cases    | 492 (≈ 0.17% — highly imbalanced)           |
| Features       | 30 (V1–V28 PCA-transformed + Time + Amount) |
| Target Column  | `Class` (0 = Normal, 1 = Fraud)             |

- Features **V1 to V28** are PCA-transformed (anonymized for privacy).
- **Time**: Seconds elapsed since the first transaction.
- **Amount**: Transaction amount.
- **Class**: 1 = Fraudulent, 0 = Legitimate.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/PrincePandit16/Credit_Card_Detection_Fraud.git
cd Credit_Card_Detection_Fraud
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Project

**Via Python script:**
```bash
python main.py
```

**Via Jupyter Notebook:**
```bash
jupyter notebook new.ipynb
```

---

## 🧰 Tech Stack

| Library        | Purpose                        |
|----------------|--------------------------------|
| `numpy`        | Numerical computations         |
| `pandas`       | Data loading and manipulation  |
| `scikit-learn` | ML models and evaluation       |
| `torch`        | Deep learning (PyTorch)        |
| `torchvision`  | PyTorch vision utilities       |
| `matplotlib`   | Data visualization             |
| `ipykernel`    | Jupyter notebook support       |

---

## 🗂 Project Structure

```
Credit_Card_Detection_Fraud/
├── creditcard.csv         # Dataset (download separately from Kaggle)
├── main.py                # Main training/inference script
├── new.ipynb              # Jupyter Notebook with analysis
├── requirements.txt       # Python dependencies
├── pyproject.toml         # Project configuration
├── uv.lock                # Lock file
├── .gitignore
└── README.md
```

---

## 📈 Approach

1. **Exploratory Data Analysis (EDA)** — Understand class imbalance and feature distributions.
2. **Preprocessing** — Normalize `Amount` and `Time`; handle class imbalance (SMOTE / undersampling).
3. **Model Training** — Train ML/DL models to classify transactions.
4. **Evaluation** — Use metrics suited for imbalanced data: Precision, Recall, F1-Score, ROC-AUC, Confusion Matrix.

---

## ⚠️ Note on Class Imbalance

The dataset is **highly imbalanced** — only ~0.17% of transactions are fraudulent. Standard accuracy is misleading. Focus on:
- **Recall** (catching actual fraud)
- **Precision** (avoiding false alarms)
- **ROC-AUC Score**

---

## 📄 License

This project is open source. The dataset is provided by the [ULB Machine Learning Group](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) and is available for research purposes.

---

## 🙋‍♂️ Author

**Prince Pandit**  
GitHub: [@PrincePandit16](https://github.com/PrincePandit16)
