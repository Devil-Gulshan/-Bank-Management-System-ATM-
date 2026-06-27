# Bank Management System 🏦

A complete desktop-based Bank Management System developed in **Java (Swing/AWT)** for the front-end user interface and **MySQL** for robust back-end database management. This application automates core banking operations such as user registration, account management, deposits, and secure authentication.

---

## 🚀 Features

* **Step-by-Step Signup:** Multi-stage digital registration form (Personal details, Additional info, and Account creation).
* **Secure Authentication:** Automated card number and secure PIN generation for login management.
* **Core Banking Transactions:** Real-time money operations including **Deposit**, **Withdrawal**, and **Balance Inquiry**.
* **Dynamic UI Layouts:** Clean desktop windows structured using Java Swing Absolute Layout positioning.

---

## 🛠️ Tech Stack

* **Frontend:** Java Swing, Java AWT
* **Backend Database:** MySQL Server
* **Database Connectivity:** JDBC (MySQL Connector/J)
* **Environment:** Windows OS (JDK 17 or higher)

---

## 📦 Database Schema Setup

To set up the required tables before running the Java application, execute the following SQL script in your MySQL instance:

```sql
CREATE DATABASE bankmanagementsystem;
USE bankmanagementsystem;

CREATE TABLE signup (
    formno VARCHAR(20), 
    name VARCHAR(20), 
    father_name VARCHAR(20), 
    dob VARCHAR(20), 
    gender VARCHAR(20), 
    email VARCHAR(30), 
    marital_status VARCHAR(20), 
    address VARCHAR(40), 
    city VARCHAR(25), 
    pincode VARCHAR(20), 
    state VARCHAR(25)
);

CREATE TABLE signuptwo (
    formno VARCHAR(20), 
    religion VARCHAR(20),
    category VARCHAR(20), 
    income VARCHAR(20), 
    education VARCHAR(20), 
    occupation VARCHAR(20), 
    pan VARCHAR(20), 
    aadhar VARCHAR(20), 
    seniorcitizen VARCHAR(20), 
    existingaccount VARCHAR(20)
);

CREATE TABLE signupthree (
    formno VARCHAR(20), 
    accountType VARCHAR(40), 
    cardnumber VARCHAR(25), 
    pin VARCHAR(10), 
    facility VARCHAR(100)
);

CREATE TABLE login (
    formno VARCHAR(20), 
    cardnumber VARCHAR(25), 
    pin VARCHAR(10)
);

CREATE TABLE bank (
    pin VARCHAR(10), 
    date VARCHAR(50), 
    type VARCHAR(20),
    amount VARCHAR(20)
);
```
---

## How to Run the Project

#1. Clone the Repository:
   git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git)
cd Bank-Management-System--master

#2. Configure Database Settings:

Open Connn.java in your IDE.
Update the MySQL connection URL, root username, and password string to match your local installation:

  connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/bankmanagementsystem", "root", "YOUR_PASSWORD");

#3. Run the Application:
   Compile and execute Login.java or Signup.java from your preferred development environment (VS Code)
