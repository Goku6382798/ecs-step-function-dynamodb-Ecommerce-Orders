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
├── architecture└── ecs-step-function-dynamodb | Ecommerce Orders
    
    │   ├── 1.png
    
    │   ├── 2.png
    
    │   └── event_driven_stepfunc_ecs.pdf
    
    ├── data
    
    │   ├── order_items_20240531.csv
    
    │   ├── order_items_20240601.csv
    
    │   ├── orders_20240531.csv
    
    │   ├── orders_20240601.csv
    
    │   └── products.csv
    
    ├── docker-commands.sh
    
    ├── docker-data-validity
    
    │   ├── app.py
    
    │   ├── Dockerfile
    
    │   └── requirements.txt
    
    ├── docker-dynamo-etl-wrangler
    
    │   ├── app.py
    
    │   ├── Dockerfile
    
    │   └── requirements.txt
    
    ├── event-pattern.json
    
    └── step-functions
    
        ├── step-function.json
        
        └── step-functions-iam-execution-policy.json



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
