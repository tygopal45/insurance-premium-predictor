# 🚀 Insurance Premium Category Predictor

A full-stack Machine Learning application that predicts the **insurance premium category** based on user details like age, BMI, income, lifestyle, and city.

---

## 🧠 Tech Stack

* **Frontend:** Streamlit
* **Backend:** FastAPI
* **Machine Learning:** Scikit-learn
* **Language:** Python

---

## 🔍 Features

* 📊 Predicts insurance premium category (Low / Medium / High)
* ⚡ Real-time prediction via FastAPI API
* 🎯 Clean and interactive UI using Streamlit
* 🧠 ML pipeline with preprocessing (ColumnTransformer + Pipeline)
* 🔄 End-to-end integration (UI → API → Model)

---

## 🏗️ Project Structure

```
.
├── main.py              # FastAPI backend
├── frontend.py          # Streamlit frontend
├── model/               # Trained ML model (if included)
├── requirements.txt     # Dependencies
├── README.md
```

---

## ⚙️ How to Run Locally

### 1️⃣ Clone the repository

```bash
git clone https://github.com/tygopal45/insurance-premium-predictor.git
cd insurance-premium-predictor
```

---

### 2️⃣ Create and activate environment

```bash
conda create -n insure python=3.10
conda activate insure
```

---

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Run FastAPI backend

```bash
python3 -m uvicorn main:app --reload
```

👉 API runs on: `http://127.0.0.1:8000`

---

### 5️⃣ Run Streamlit frontend

```bash
streamlit run frontend.py
```

👉 App runs on: `http://localhost:8501`

---

## 🔗 API Endpoint

### POST `/predict`

#### Input:

```json
{
  "age": 30,
  "weight": 65,
  "height": 1.7,
  "income_lpa": 10,
  "smoker": false,
  "city": "Mumbai",
  "occupation": "private_job"
}
```

#### Output:

```json
{
  "predicted_category": "Medium"
}
```

---

## 🧠 ML Pipeline

* Feature Engineering:

  * BMI calculation
  * Age grouping
  * Lifestyle risk scoring
  * City tier mapping

* Preprocessing:

  * OneHotEncoding for categorical features
  * Numeric features passed directly

* Model:

  * RandomForestClassifier

---

## 🎯 Future Improvements

* 🌐 Deploy on cloud (Render / AWS / HuggingFace)
* 📈 Add probability/confidence scores
* 🧾 Save prediction history
* 🎨 Improve UI/UX

---

## 👨‍💻 Author

**Gopal Jee**
