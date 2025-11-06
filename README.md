# 🚗 Car Rental System  
*A complete web and database management system for online vehicle rentals.*

![Repo Size](https://img.shields.io/github/repo-size/Valgha/Car-Rental-System?color=blue&style=flat-square)
![Languages](https://img.shields.io/github/languages/count/Valgha/Car-Rental-System?color=green&style=flat-square)
![Top Language](https://img.shields.io/github/languages/top/Valgha/Car-Rental-System?color=orange&style=flat-square)
![Contributors](https://img.shields.io/github/contributors/Valgha/Car-Rental-System?color=yellow&style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)
![Status](https://img.shields.io/badge/Project%20Status-Completed-brightgreen?style=flat-square)
![Database](https://img.shields.io/badge/Database-MySQL-blue?style=flat-square)
![Backend](https://img.shields.io/badge/Backend-PHP-yellow?style=flat-square)
![Frontend](https://img.shields.io/badge/Frontend-HTML%20%7C%20CSS-purple?style=flat-square)

---

## 🧭 Overview  
The **Car Rental System** is a full-stack project designed to streamline car rental operations — from registering customers and managing vehicles to handling bookings, payments, and generating reports.

Built with **PHP, MySQL, HTML, and CSS**, this project demonstrates complete CRUD operations, relational database design, and a user-friendly web interface.

---

## 🧩 Features  

### 👥 Customer Management  
- Register and manage customer information.  
- Track membership, discounts, and rental history.  

### 🚘 Vehicle Management  
- Add and update cars with type, model, and rates.  
- Manage vehicle availability (daily and weekly rates).  
- Link cars to respective owners.  

### 📅 Rental Operations  
- Create and manage rental bookings.  
- Automatically find available vehicles by type and date.  
- Process returns with total billing calculation (driver fees, deposit, discount).  

### 🧾 Billing & Payment  
- Generate bills dynamically for each rental.  
- Adjust deposits and apply membership discounts.  
- Add chauffeur charges when applicable.  

### 📊 Reports & Analytics  
- Generate weekly earning reports:  
  - By **owner**  
  - By **car type**  
  - By **individual car**  

### 💬 Feedback System  
- Collect and store customer feedback linked to service employees.  

---

## 🧱 System Architecture  

The project includes two key components:  

1. **Database Layer (MySQL)**  
   - Defined in [`Create_Tables.sql`](./CarRental/Create_Tables.sql).  
   - Contains all tables, relationships, and constraints for cars, owners, customers, rentals, and billing.  

2. **Application Layer (PHP + HTML + CSS)**  
   - Located in [`CarRental`](./CarRental).  
   - Implements data entry forms and interactive reports.  

---

## 🗄️ Database Schema Overview  

**Key Entities:**  
- `CAR` – Stores vehicle info and rates.  
- `CUSTOMER` – Maintains customer data and membership details.  
- `RENTAL` – Tracks rental records.  
- `DAILY`, `WEEKLY` – Subclasses of rental periods.  
- `DRIVER`, `SELF`, `CHAUFFEUR` – Driving options.  
- `OWNER`, `OWNS` – Ownership relationships.  
- `BILL` – Payment records.  
- `FEEDBACK` – Customer reviews.  

**Relationships:**  
- `OWNER` → `CAR` — **1:N**  
- `CUSTOMER` → `RENTAL` — **1:1**  
- `RENTAL` → (`DAILY`, `WEEKLY`) — **ISA hierarchy**  
- `DRIVER` → (`SELF`, `CHAUFFEUR`) — **ISA hierarchy**  
- `CAR` → `OWNER` via `OWNS`  

📄 See **Schema_Diagram.pdf** for the complete EER diagram.

---

## ⚙️ Installation & Setup  

###  Clone the Repository  
```bash
git clone https://github.com/Valgha/Car-Rental-System.git
cd Car-Rental-System/CarRental




