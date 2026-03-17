# 🚀 AWS Elastic Beanstalk + RDS + EC2 Project

## 📌 Project Overview
This project demonstrates how to deploy a web application using AWS Elastic Beanstalk, create an RDS database, and securely access it from an EC2 instance within the same VPC.

---

## 🏗️ Architecture
- Elastic Beanstalk → Application Deployment
- Amazon RDS (MySQL) → Database
- EC2 Instance → Database Client
- VPC → Networking (Public & Private Subnets)
- Security Groups → Controlled Access

---

## ⚙️ Technologies Used
- AWS Elastic Beanstalk  
- Amazon RDS (MySQL)  
- Amazon EC2  
- VPC / Subnets / Security Groups  
- Amazon Linux 2023  
- MariaDB Client  

---

## 🔧 Step-by-Step Implementation

### 1. Elastic Beanstalk Setup
- Created application environment
- Deployed sample application
- Configured IAM roles

### 2. RDS Database Setup
- Enabled database during environment creation
- Engine: MySQL
- Instance type: db.t3.micro
- Storage: 20GB
- Deployed inside private subnet

### 3. EC2 Instance Setup
- Launched EC2 in public subnet
- Installed MariaDB client
- Connected to RDS using endpoint

### 4. Security Configuration
- Allowed MySQL (3306) access from EC2 security group only
- Ensured RDS is not publicly accessible

---

## 🧪 Database Testing

```sql
CREATE DATABASE internship;
USE internship;

CREATE TABLE users (
id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(50)
);

INSERT INTO users(name) VALUES ('Sanket');

SELECT * FROM users;