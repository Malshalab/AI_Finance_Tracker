# 📝 Project Requirements Document: Personal Finance Tracker with AI Insights

## 1️⃣ Project Overview
A **full-stack personal finance tracker** to help users log their income and expenses, visualize spending trends, and receive **ML-powered budgeting recommendations**.  
This project integrates a modern React/TypeScript frontend, Java Spring Boot (or Python FastAPI) backend, an ML microservice, and is deployed on AWS using Docker and Kubernetes.

---

## 2️⃣ Functional Requirements

### ✅ User Management
- Secure user registration and login.
- JWT-based authentication for all routes.

### ✅ Transactions
- Create, view, update, and delete transactions.
- Transactions include:  
  - Amount  
  - Type (income/expense)  
  - Category (groceries, rent, etc.)  
  - Date, description, and optional tags.

### ✅ Dashboard
- Summaries of income & expenses.
- Interactive charts for spending patterns and trends.
- Monthly/weekly views.

### ✅ ML-Powered Insights
- ML API predicts next month’s budget based on spending history.
- Alerts for overspending or budget thresholds.
- Integration with backend & frontend for real-time insights.

---

## 3️⃣ Non-Functional Requirements

- ⚡ **Performance**: API response < 200ms; ML prediction latency < 500ms.
- 🔒 **Security**:  
  - HTTPS for deployment  
  - Secure password storage (bcrypt)  
  - JWT-based authentication
- 🔗 **Scalability**:  
  - Use Docker & K8s for microservice orchestration.  
  - Separate services for frontend, backend, and ML microservice.
- 📝 **Documentation**:  
  - Clean README, architecture diagrams, and API docs (Swagger/OpenAPI).

---

## 4️⃣ Tech Stack

| Layer             | Technology                             |
|-------------------|----------------------------------------|
| **Frontend**      | React (with TypeScript), Tailwind CSS  |
| **Backend**       | Java (Spring Boot) or Python (FastAPI) |
| **Database**      | PostgreSQL                             |
| **ML Microservice**| Python (Flask/FastAPI, scikit-learn)   |
| **DevOps**        | Docker, Kubernetes, GitHub Actions     |
| **Cloud**         | AWS (EC2, S3, IAM roles)               |
| **Charts**        | Chart.js or Recharts                   |

---

## 5️⃣ Data Models

### **User**
- `id`, `username`, `email`, `hashed_password`, `created_at`

### **Transaction**
- `id`, `user_id`, `amount`, `type` (income/expense), `category`, `date`, `description`, `tags`

### **ML Insights**
- Predicted budget, category-specific suggestions

---

## 6️⃣ High-level API Endpoints

### 🔹 Auth APIs
- `POST /api/auth/register`  
- `POST /api/auth/login`  

### 🔹 Transactions APIs
- `GET /api/transactions`  
- `POST /api/transactions`  
- `PUT /api/transactions/{id}`  
- `DELETE /api/transactions/{id}`  

### 🔹 ML Insights APIs
- `GET /api/ml/budget-recommendation`  

### 🔹 User APIs
- `GET /api/user/profile`  

---

## 7️⃣ Deployment Plan

- Local development: Docker Compose stack (backend, frontend, DB, ML microservice).  
- Cloud:  
  - AWS EC2 for initial deployment  
  - Kubernetes (Minikube locally, AWS EKS optional)  
- CI/CD: GitHub Actions for linting, testing, and deployment.

---

## 8️⃣ Stretch Goals & Future Enhancements

- Multi-currency support.  
- Notifications (email or SMS).  
- Integration with third-party APIs (e.g., Plaid, budgeting APIs).  
- Blockchain-based transaction logs for transparency.  
- AI-driven financial goal tracking.

---

## 9️⃣ Timeline (High-level)

| Phase | Tasks                                          | Duration  |
|-------|-------------------------------------------------|-----------|
| 1     | Backend API, Auth, DB schema                   | Days 1-15 |
| 2     | Frontend + data viz                            | Days 16-30|
| 3     | Docker, K8s, AWS deployment                    | Days 31-45|
| 4     | ML insights, integration & final polish        | Days 46-60|

---

### 🚀 Final Deliverables
✅ A complete **Personal Finance Tracker** app with ML insights.  
✅ Full documentation (architecture diagrams, README, demo video).  
✅ Clean, scalable, cloud-deployed code ready for **real-world use**!

---

### 📝 Notes
This document is **living**—update it as you build new features, refine the architecture, or pivot. Let’s make this project a highlight of your portfolio! 🚀✨
