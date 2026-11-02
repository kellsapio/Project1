# Loki Café - Stock Inventory System

A simple console-based inventory and stock management system written in Python.  
It supports **Admin** and **Staff** modes with role-based dashboards, inventory tracking, delivery records, expiration alerts, and shift handover reports.

---

## Features

### Main Menu
* **Login** — Role-based authentication (Admin / Staff)
* **Exit System** — Closes the program

### Admin Menu
1. View All Stock Levels
2. View Delivery Records Table
3. Add New Ingredient
4. Stock Adjustment (+/-)
5. Remove Ingredient
6. Record Incoming Delivery
7. Filter Stock Alert
8. View Shift Handover Reports
9. Register New Staff Account
10. Logout

### Staff Menu
1. View All Stock Levels
2. View Delivery Records Table
3. Deduct Stock Usage
4. Record Incoming Delivery
5. Filter Stock Alerts
6. Log Shift Handover Report
7. Logout

---

## Default Login (System Accounts)

| Role | Username | Password |
| :--- | :--- | :--- |
| **Admin** | `admin` | `admin123` |
| **Staff** | `loki` | `loki123` |

---

## Default Inventory Items

| ID | Ingredient Name | Qty | Unit | Min Level | Expiration | Status |
| :-: | :--- | :-: | :-: | :-: | :-: | :--- |
| 1 | Espresso Beans | 10 | kg | 3 | 2026-10-15 | Safe |
| 2 | Dairy Cream | 2 | L | 5 | 2026-10-05 | Expired |
| 3 | Caramel Syrup | 4 | L | 2 | 2026-12-01 | Safe |
| 4 | Fresh Milk | 1 | L | 5 | 2026-10-12 | Low Stock / Expiring |

---

## How to Run

1. Make sure you have **Python 3** installed.
2. Save the code as a `.py` file (e.g., `inventory.py`).
3. Run it in your terminal/command prompt:
   ```bash
   python inventory.py

or

python3 inventory.py

Key Behaviors
1. Stock management: Admins can adjust, add, or remove stock, while staff can deduct stock usage.
2. Smart status tracking: Automatically detects item statuses such as Safe, Low Stock, Expired, and Expiring Soon (within 7 days).
3. Delivery management: Keeps a separate table and history for incoming deliveries and batch tracking.
4. Role-based access: Restricts features based on logged-in account (Admin vs Staff).
5. Input validation: Ensures positive numbers for quantities and proper YYYY-MM-DD formats for expiration dates.

Project Structure (Single File)

All data is kept in memory using Python lists:
1. users
2. inventory
3. delivery_records
4. shift_handover_reports

No external libraries or database are required — only the Python standard library (sys and datetime).

Notes:
1. Data is not persisted. Everything resets when you close the program.
2. This is a console / terminal application (text-based interface).
3. Designed for simple classroom / project demonstration purposes.

Author

Created as a student project.
Feel free to improve it (add file saving, better UI, etc.).
