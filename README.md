# 🌍 CU Kasol Trip Form

Welcome to the **CU Kasol Trip Form** repository! This project is a simple yet effective PHP-based web form designed to collect participant details for the CU Kasol Trip and store them in a MySQL database via phpMyAdmin.

---

## 🚀 Features
✅ User-friendly registration form with HTML, CSS, and PHP.<br>
✅ Secure data storage in a MySQL database using phpMyAdmin.<br>
✅ Instant confirmation message upon form submission.<br>
✅ Responsive and visually appealing UI.<br>
✅ Automatic timestamping of form submissions.

---

## 📝 How It Works
1. A user fills out the form by entering their **name, age, gender, email, phone number, and additional details**.
2. When the **Submit** button is clicked, the form data is sent to `index.php` using the **POST** method.
3. PHP processes the data and stores it in a MySQL database using **phpMyAdmin**.
4. The submission includes a **timestamp**, recording the exact date and time when the form was submitted (e.g., `2025-02-14 12:39:57`).
5. Upon successful submission, a **confirmation message** is displayed: 
   
   _"Thanks for submitting your form. We are happy to see you joining us for the Kasol trip."_

---

## 🛠 Installation Guide
### Step 1: Clone the Repository
```sh
   git clone https://github.com/RamitRoshan/cu-kasol-trip-form.git
```

### Step 2: Set Up XAMPP
1. Download and install **XAMPP** from [Apache Friends](https://www.apachefriends.org/).
2. Open **XAMPP Control Panel** and **start** both **Apache** and **MySQL** services.

### Step 3: Configure the Database
1. Open **phpMyAdmin** by visiting `http://localhost/phpmyadmin/`.
2. Create a database named `trip`.
3. Import the provided `database.sql` file to create the necessary tables.

### Step 4: Update Database Credentials
Modify `index.php` to match your MySQL username and password.

### Step 5: Run the Project
1. Place the project folder inside the `htdocs` directory of XAMPP.
2. Open a web browser and visit:
   ```sh
   http://localhost/cu-kasol-trip-form/index.php
   ```

---

## 🗄 Database Structure
```sql
CREATE DATABASE trip;
USE trip;

CREATE TABLE trip (
    sno INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    gender VARCHAR(10),
    email VARCHAR(100),
    phone VARCHAR(15),
    other TEXT,
    dt TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

## 📁 Project Structure
```
cu-kasol-trip-form/
|-- index.php         # Main PHP script
|-- style.css         # Stylesheet for UI
|-- index.js          # JavaScript file (if required)
|-- bg.jpg           # Background image
|-- README.md         # Documentation
|-- database.sql      # SQL script for the database
```

## Made by ❤️ Ramit Roshan
Happy coding! 🎉

