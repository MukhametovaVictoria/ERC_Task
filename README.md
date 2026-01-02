# Utility Meter Reading & Billing Service

**A simple ASP.NET Core MVC service for recording utility meter readings and generating billing information.**

---

## 🔎 Overview

This project implements a backend service that allows users to submit utility meter readings and automatically calculates billing based on the latest submitted data.

It was created as part of a technical task to demonstrate backend development skills using **ASP.NET Core MVC**, **Entity Framework**, and **MS SQL Server**.

---

## 🛠 Features

The service includes:

- 📥 Recording meter readings for a personal account
- 💰 Automatic billing generation when a new reading is submitted
- 🧩 Four domain models representing core entities
- REST-style architecture with separate controllers for each model

---

## 🧱 Models & Their Responsibilities

1. **User** — account owner  
2. **PersonalAccount** — utility account linked to a user  
3. **MetersData** — utility meter readings  
4. **Bill** — generated billing document

Each model has a dedicated controller that handles CRUD operations and business logic.

---

## 🚦 Business Rules

- A *User* must be created together with a *PersonalAccount*.  
- Duplicate accounts or users are not allowed.  
- *PersonalAccount* owner cannot be changed after creation.  
- Meter readings can only be updated for the most recent month.  
- Every time meter readings are submitted, a **Bill** is automatically generated or updated.  
- Simple validation is implemented for basic scenarios.

---

## 🧩 Tech Stack

- **Backend**: ASP.NET Core MVC  
- **ORM**: Entity Framework Core  
- **Database**: MS SQL Server  
- **Patterns**: REST-style controllers, layered architecture

---

## 🚀 How to Run (Example)

1. Clone the repository  
2. Configure the connection string in `appsettings.json`  
3. Run `dotnet ef database update` to apply migrations  
4. Start the application with `dotnet run`  
5. Use Swagger or Postman to test API endpoints

---

## 📈 What This Demonstrates

This repository highlights practical skills in:

✔ Building a web backend with .NET MVC  
✔ Designing relational data models  
✔ Handling business logic and validation  
✔ Working with Entity Framework and SQL Server

---

## 🧠 Next Improvements (optional)

- Add authentication and authorization  
- Add automated tests  
- Deploy as a Docker container or to cloud

---
