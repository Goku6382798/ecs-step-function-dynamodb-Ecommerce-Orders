# ECS + Step Functions + DynamoDB | Ecommerce Orders

This project demonstrates an **event-driven data pipeline** for an e-commerce orders system.  
It uses **Amazon ECS** to run containerized tasks, **AWS Step Functions** for orchestration, and **DynamoDB** for storing processed order data.  
The setup also includes Dockerized services for data validation and ETL transformations, along with sample order datasets.

---

## 📊 Architecture

![Architecture](ecs-step-function-dynamodb%20%7C%20Ecommerce%20Orders/architecture/1.png)  
![Workflow](ecs-step-function-dynamodb%20%7C%20Ecommerce%20Orders/architecture/2.png)

---

## 📂 Project Structure

ecs-step-function-dynamodb | Ecommerce Orders
│
├── architecture
│ ├── 1.png # Architecture diagram
│ ├── 2.png # Workflow diagram
│ └── event_driven_stepfunc_ecs.pdf # Detailed documentation
│
├── data
│ ├── order_items_20240531.csv # Order items dataset (May 31, 2024)
│ ├── order_items_20240601.csv # Order items dataset (June 01, 2024)
│ ├── orders_20240531.csv # Orders dataset (May 31, 2024)
│ ├── orders_20240601.csv # Orders dataset (June 01, 2024)
│ └── products.csv # Products dataset
│
├── docker-commands.sh # Helper script for Docker setup
│
├── docker-data-validity
│ ├── app.py # Validation service app
│ ├── Dockerfile # Dockerfile for validation service
│ └── requirements.txt # Dependencies for validation service
│
├── docker-dynamo-etl-wrangler
│ ├── app.py # ETL service app
│ ├── Dockerfile # Dockerfile for ETL service
│ └── requirements.txt # Dependencies for ETL service
│
├── event-pattern.json # EventBridge pattern for triggering
│
└── step-functions
├── step-function.json # Step Function state machine definition
└── step-functions-iam-execution-policy.json # IAM policy for Step Functions execution


---

## ⚙️ Tech Stack
- **Amazon ECS** – Containerized ETL + validation tasks  
- **AWS Step Functions** – Orchestration of event-driven workflows  
- **Amazon DynamoDB** – Scalable NoSQL data store  
- **Amazon EventBridge** – Event-driven triggers  
- **Docker** – Local service containerization  

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   https://github.com/Goku6382798/ecs-step-function-dynamodb-Ecommerce-Orders
   cd "ecs-step-function-dynamodb | Ecommerce Orders"
