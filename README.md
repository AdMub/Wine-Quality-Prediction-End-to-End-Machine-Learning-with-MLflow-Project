# 🍷 Wine Quality Prediction – End-to-End Machine Learning with MLflow & MLOps  

![Build Status](https://img.shields.io/github/actions/workflow/status/AdMub/Wine-Quality-Prediction-End-to-End-Machine-Learning-with-MLflow-Project/ci-cd.yml?branch=main&label=CI%2FCD%20Build&logo=github)  
![Docker](https://img.shields.io/badge/Docker-Ready-blue?logo=docker)  
![AWS](https://img.shields.io/badge/Deployed%20on-AWS-orange?logo=amazon-aws)  
![MLflow](https://img.shields.io/badge/MLflow-Tracking%20Enabled-blue?logo=mlflow)  
![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)  
![License](https://img.shields.io/github/license/AdMub/Wine-Quality-Prediction-End-to-End-Machine-Learning-with-MLflow-Project)  

---
 

## 📌 Project Overview  
This project implements an **end-to-end MLOps pipeline** for predicting wine quality using **ElasticNet Regression**. It leverages **MLflow for experiment tracking**, **DagsHub for model registry**, and **GitHub Actions CI/CD** for automation. The final model is containerized with **Docker** and deployed on **AWS** for scalable inference.  

The solution integrates **data processing, model training, experiment tracking, continuous integration, continuous delivery, and deployment** – demonstrating a modern MLOps workflow.  

---

## 🚀 Tech Stack & Tools  

- **Programming:** Python  
- **Model:** ElasticNet Regression (hyperparameter fine-tuning)  
- **Experiment Tracking:** MLflow + DagsHub  
- **Deployment:** Flask Web App (HTML, CSS, Bootstrap, JavaScript)  
- **CI/CD:** GitHub Actions (Testing, Linting, Docker Build & Push, AWS Deploy)  
- **Containerization:** Docker  
- **Cloud:** AWS (for hosting and serving model)  
- **Version Control:** GitHub  

---

## 📊 Dataset  

The dataset contains physicochemical tests of wine and their corresponding quality scores (0–10).  

**Features include:**  
- Fixed acidity  
- Volatile acidity  
- Citric acid  
- Residual sugar  
- Chlorides  
- Free sulfur dioxide  
- Total sulfur dioxide  
- Density  
- pH  
- Sulphates  
- Alcohol  

**Target:**  
- `quality` (Wine Quality Score)  

Sample of the dataset:  

| fixed acidity | volatile acidity | citric acid | residual sugar | chlorides | free sulfur dioxide | total sulfur dioxide | density | pH  | sulphates | alcohol | quality |
|---------------|-----------------|-------------|----------------|-----------|----------------------|-----------------------|---------|-----|------------|---------|---------|
| 7.4           | 0.70            | 0.00        | 1.9            | 0.076     | 11.0                 | 34.0                  | 0.9978  | 3.51| 0.56       | 9.4     | 5       |
| 7.8           | 0.88            | 0.00        | 2.6            | 0.098     | 25.0                 | 67.0                  | 0.9968  | 3.20| 0.68       | 9.8     | 5       |
| 11.2          | 0.28            | 0.56        | 1.9            | 0.075     | 17.0                 | 60.0                  | 0.9980  | 3.16| 0.58       | 9.8     | 6       |

---

## 🏗️ Project Architecture  

**Pipeline Steps:**  
1. **Data Ingestion & Preprocessing**  
2. **Model Training (ElasticNet)**  
3. **Hyperparameter Tuning**  
4. **Experiment Tracking with MLflow**  
5. **Model Registry on DagsHub**  
6. **CI/CD with GitHub Actions**  
   - Linting & Testing  
   - Build Docker Image  
   - Push to DockerHub/AWS ECR  
   - Deploy on AWS  
7. **Web Application (Flask + Bootstrap + JavaScript)**  
8. **Containerization & Deployment**  


---

## ⚙️ Setup Instructions  

### 1️⃣ Clone Repository  
```bash
git clone https://github.com/AdMub/Wine-Quality-Prediction-End-to-End-Machine-Learning-with-MLflow-Project.git
cd Wine-Quality-Prediction-End-to-End-Machine-Learning-with-MLflow-Project
```

### 2️⃣ Create Environment
```bash
conda create -n wine-mlops python=3.9 -y
conda activate wine-mlops
pip install -r requirements.txt
```

### 3️⃣ Run MLflow Tracking Server
```bash
mlflow ui
```
Access at: `http://127.0.0.1:5000`

### 4️⃣ Run Flask App Locally
```bash
python app.py
```
Access at: `http://127.0.0.1:8080`

### 5️⃣ Run with Docker
```bash
docker build -t wine-mlops .
docker run -p 8080:8080 wine-mlops
```

---

## 🔄 CI/CD Workflow

This project uses **GitHub Actions** for automation:
- ✅ Code linting & testing
- 🐳 Build & push Docker image
- ☁️ Deploy to AWS
- 
<img width="1422" height="296" alt="CI-CD" src="https://github.com/user-attachments/assets/dae2424c-96cd-4542-8e85-e1b434def7cc" />


---

## 🌐 Deployment
The Flask web app allows users to input wine physicochemical properties and get a predicted **wine quality score.**

<img width="1910" height="883" alt="form" src="https://github.com/user-attachments/assets/ba5e3ae6-c8f2-42d4-b366-3b3d9d2bf23a" />


<img width="1920" height="913" alt="result" src="https://github.com/user-attachments/assets/e24050c2-0e5e-4ef3-9796-d50aeabf3b97" />


---

## 📈 Results & Model Performance
- **Algorithm:** ElasticNet Regression
- **Best Parameters:** (alpha, l1_ratio) from hyperparameter tuning
- **Evaluation Metrics:**
  - **R² Score:** `0.30008849924745673`
  - **RMSE:** `0.7033193291172796`
  - **MAE:** `0.557398274512252`



---

## 🐳 Docker & AWS
- **Dockerized App** ensures reproducibility.
- **AWS Deployment** provides scalable inference


---

## 📂 Repository Structure

```bash
Wine-Quality-Prediction-End-to-End-Machine-Learning-with-MLflow-Project
│── data/                     # Dataset
│── notebooks/                # Jupyter notebooks for exploration
│── src/                      # Source code (data, model, utils, etc.)
│── app.py                    # Flask application
│── Dockerfile                # Docker image definition
│── requirements.txt          # Python dependencies
│── .github/workflows/        # GitHub Actions CI/CD pipeline
│── mlruns/                   # MLflow experiment logs
│── README.md                 # Project documentation
```

---

## 📜 Future Work
- Add support for advanced models (Random Forest, XGBoost, Deep Learning)
- Deploy on Kubernetes for large-scale serving
- Integrate monitoring tools (Prometheus, Grafana)
  
---

## 🙌 Acknowledgements  

- **Dataset:** [Wine Quality Data Set](https://archive.ics.uci.edu/dataset/186/wine+quality) – UCI Machine Learning Repository  
- **MLOps Inspiration:** Open-source community projects, tutorials, and best practices in modern ML engineering  

### 💡 Contributions, issues, and feature requests are welcome!  
Feel free to fork this repository and submit a pull request.  

---

## 👨‍💻 Author  

**Mubarak Adisa**  
- 🎓 Civil Engineering + Computer Science (Data Science & AI Focus)  
- 🔗 GitHub: [AdMub](https://github.com/AdMub)  
- 💼 LinkedIn: [Mubarak Adisa](https://www.linkedin.com/in/mubarak-adisa-334a441b6/)  



