# REAL-ESTATE-PRICE-PREDICTION-SYSTEM-Production-Ready-.
This repository contains a data  including datasets, preprocessing, EDA, visualizations, and insights using Python.
# 🏠 Real Estate Price Prediction System (Production-Ready ML Pipeline)

## 🚀 Project Overview

This project is a **production-ready end-to-end Machine Learning system** that predicts real estate prices using advanced models and modern MLOps practices.

It goes beyond a basic ML model by implementing:

* Automated data pipeline
* Multiple model training (XGBoost + Neural Networks)
* Model evaluation and selection
* REST API for predictions (FastAPI)
* Interactive dashboard (Streamlit)
* Containerized deployment (Docker)
* Monitoring and logging
* CI/CD pipeline
* Testing framework

---

# 🎯 Business Problem

Real estate pricing is complex and influenced by multiple factors such as location, size, and property features.

Manual pricing:

* ❌ Inconsistent
* ❌ Time-consuming
* ❌ Prone to bias

This system provides **accurate, data-driven price predictions** to support:

* Real estate agencies
* Property investors
* Buyers and sellers

---

# 🧠 System Architecture

```id="s9z5od"
          ┌──────────────┐
          │   Raw Data   │
          └──────┬───────┘
                 │
        Data Ingestion
                 │
        Data Preprocessing
                 │
        Feature Engineering
                 │
       Model Training (XGB + NN)
                 │
        Model Evaluation
                 │
        Model Registry (MLflow)
                 │
     ┌───────────┴───────────┐
     │                       │
 FastAPI Backend      Streamlit Dashboard
     │                       │
     └───────────┬───────────┘
                 │
          User Predictions
```

---

# 📂 Project Structure

```id="c91y8c"
real_estate_ml_system/

├── data/
│   ├── raw/
│   ├── processed/
│
├── notebooks/
│   └── eda.ipynb
│
├── src/
│   ├── data_pipeline/
│   │   ├── ingest.py
│   │   ├── preprocess.py
│   │
│   ├── models/
│   │   ├── train.py
│   │   ├── evaluate.py
│   │   ├── registry.py
│   │
│   ├── api/
│   │   └── main.py
│   │
│   ├── dashboard/
│   │   └── app.py
│   │
│   ├── monitoring/
│   │   └── logger.py
│
├── tests/
│   ├── test_pipeline.py
│   ├── test_model.py
│
├── docker/
│   ├── Dockerfile
│   └── docker-compose.yml
│
├── requirements.txt
├── README.md
```

---

# ⚙️ Tech Stack

### Programming

* Python

### Data Processing

* Pandas, NumPy

### Machine Learning

* Scikit-learn
* XGBoost
* TensorFlow / Keras

### Backend API

* FastAPI

### Frontend Dashboard

* Streamlit

### MLOps & Tools

* MLflow (Model Tracking)
* Docker (Containerization)
* Pytest (Testing)

---

# 🔄 ML Pipeline

## 1. Data Ingestion

* Loads raw dataset from CSV

## 2. Data Preprocessing

* Handles missing values
* Encodes categorical variables
* Splits features and target

## 3. Model Training

* XGBoost Regressor
* Neural Network (Dense layers)

## 4. Model Evaluation

* R² Score
* RMSE

## 5. Model Registry

* Stores trained models using MLflow

---

# 🤖 Model Performance

| Model          | Metric | Score  |
| -------------- | ------ | ------ |
| XGBoost        | R²     | ~0.85+ |
| Neural Network | R²     | ~0.80+ |

*(Values depend on dataset)*

---

# 🌐 API (FastAPI)

### Endpoint

```id="c54b0x"
POST /predict
```

### Request

```id="2t5l0g"
{
  "area": 2000,
  "bedrooms": 3,
  "bathrooms": 2
}
```

### Response

```id="c5txhg"
{
  "predicted_price": 7500000
}
```

---

# 📊 Dashboard (Streamlit)

Features:

* User input form
* Real-time predictions
* Visualization of price trends

Run dashboard:

```id="5gcrx7"
streamlit run src/dashboard/app.py
```

---

# 🐳 Docker Deployment

## Build Container

```id="3o5xfh"
docker-compose up --build
```

Services:

* FastAPI → `localhost:8000`
* Streamlit → `localhost:8501`

---

# 📈 Monitoring & Logging

* Logs stored in `logs/app.log`
* Tracks:

  * Input data
  * Predictions
  * Errors

---

# 🔁 CI/CD Pipeline

GitHub Actions pipeline:

* Install dependencies
* Run tests
* Validate build

---

# 🧪 Testing

Run tests:

```id="ffb6ib"
pytest
```

Includes:

* Pipeline tests
* Model validation tests

---

# 🚀 How to Run Locally

## 1️⃣ Clone Repo

```id="9md9jo"
git clone https://github.com/yourusername/real-estate-ml-system.git
```

---

## 2️⃣ Setup Environment

```id="x8qil5"
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

---

## 3️⃣ Train Model

```id="2cijmb"
python src/data_pipeline/ingest.py
python src/data_pipeline/preprocess.py
python src/models/train.py
```

---

## 4️⃣ Run API

```id="6avb0c"
uvicorn src.api.main:app --reload
```

---

## 5️⃣ Run Dashboard

```id="71mwuj"
streamlit run src/dashboard/app.py
```

---

# 🔮 Future Improvements

* Hyperparameter tuning (GridSearchCV / Optuna)
* Feature engineering pipelines
* Real-time data ingestion APIs
* Cloud deployment (AWS / GCP)
* Kubernetes orchestration
* Model drift detection

---

# 👨‍💻 Author

**Ranganathan**
Data Analyst → Transitioning to Data Scientist

---

# ⭐ If You Found This Useful

Give this repo a ⭐ and share it.
