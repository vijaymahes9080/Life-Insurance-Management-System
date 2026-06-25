# Life Insurance Management System (LIMS)

[![PHP Version](https://img.shields.io/badge/php-%3E%3D%205.5-blue.svg)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/database-MySQL-orange.svg)](https://www.mysql.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A comprehensive web-based management portal designed to streamline operations for Life Insurance providers. The portal manages agents, clients, policies, nominees, and premium payment records with distinct access control levels and structured data integrity.

---

## 🚀 Key Features

*   **Multilevel Access Control**: Role-based access for Master Agents (Admins), Agents, and Clients.
*   **Agent Management**: Administrators can register, view, update, and remove agents from different branches.
*   **Client Management**: Agents can create and maintain client records, including profile photo uploads. Data ownership rules ensure agents can only edit or delete client records they personally registered.
*   **Nominee Directory**: Link client policies to one or more nominees with specific relationships, priority levels, and personal details.
*   **Policy Linkage**: Assign policies containing distinct terms and payout percentages to clients.
*   **Premium Payments Tracking**: Record monthly premium payments, track outstanding dues, calculate late-payment fines, and generate printable receipts.
*   **Client Self-Service Dashboard**: Clients can log in to view their active policy details, nominee information, and premium transaction history.

---

## 📊 Database Architecture

The application relies on a MySQL schema composed of five core tables:

1.  **`agent`**: Stores credentials and branch information for insurance agents.
2.  **`client`**: Contains personal information, associated policy references, parent agent IDs, and profile images.
3.  **`nominee`**: Holds details of beneficiaries linked to a specific client.
4.  **`policy`**: Details individual insurance policies, terms (duration), and payout percentages.
5.  **`payment`**: Tracks financial ledger items for premium payments, fines, and due balances.

---

## 🛠️ Technology Stack

*   **Backend**: PHP
*   **Database**: MySQL / MariaDB
*   **Frontend**: HTML5, CSS3, JavaScript (enhanced with Bootstrap-based dashboard widgets and styles)

---

## 📦 Setup & Installation on Localhost

To deploy this project locally using a stack like **XAMPP**, follow these steps:

### 1. Clone the Repository
Clone the codebase into your local web server root directory (e.g., `xampp/htdocs/`):
```bash
git clone https://github.com/vijaymahes9080/Life-Insurance-Management-System.git
```

### 2. Configure Database Connection
Open `connection.php` and configure your local MySQL credentials:
```php
$servername = "localhost";
$username   = "YOUR_DATABASE_USERNAME"; // Default is usually "root"
$password   = "YOUR_DATABASE_PASSWORD"; // Default is usually ""
$dbname     = "lims";
```

### 3. Import Database Schema
1. Start the **Apache** and **MySQL** services in your XAMPP Control Panel.
2. Open your web browser and navigate to [http://localhost/phpmyadmin](http://localhost/phpmyadmin).
3. Create a new database named `lims`.
4. Click on the **Import** tab, select the backup file located at `database/lims.sql` in this repository, and click **Go**.

### 4. Run the Application
Access the portal by navigating to:
[http://localhost/Life-Insurance-Management-System](http://localhost/Life-Insurance-Management-System) (or the corresponding directory name where the code is cloned).

---

## 🔑 Default Credentials for Evaluation

| User Type | Username | Password |
| :--- | :--- | :--- |
| **Master Agent (Admin)** | `admin` | `12345` |
| **Agent** | `555` | `666` |
| **Client** | `1511986023` | `123` |
