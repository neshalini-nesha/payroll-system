# payroll-system
Payroll system assessment. 
This is a web-based Payroll Management application. It allows you to manage Departments and Employees, calculate monthly payroll (including Tax and EPF), and generate downloadable PDF payslips.

🚀 How to Run This System (Step-by-Step)

Follow these steps exactly to get the system running on your local computer.
1. Prerequisites
Ensure you have the following installed:
*   **PHP** (8.1 or higher)
*   **Composer** (PHP dependency manager)

2. Download and Setup
Clone/Download** this repository to your computer.
Open your **Terminal** or **Command Prompt** and navigate into the project folder.
Run the following command to install the necessary libraries:
    ```bash
    composer install
    ```

3. Environment Configuration
1.  In the project folder, find the file named `payroll_system`.
2.  **Rename** it to simply `.env`.
3.  Back in your terminal, run this command to generate a unique security key:
    ```bash
    php artisan key:generate
    ```

4. Database Setup (SQLite)
This system uses **SQLite**, which means you don't need to install a separate database server.
1.  Inside the `database` folder, create a new empty file named `database.sqlite`.
2.  Now, run the following command to build the tables (Departments, Employees, etc.):
    ```bash
    php artisan migrate:fresh
    ```

5. Start the Application
Run the start command:
    ```bash
    php artisan serve
    ```
   Open your web browser and go to:[http://127.0.0.1:8000]

---

🔐 How to Log In (Credentials)

Because the database starts empty for your security and testing:
1.  Click on Register on the login screen.
2.  Create any account (e.g., Name: "Admin", Email: "admin@test.com", Password: "123456").
3.  Once registered, use those same details to **Log In**.
4.  You can now access the Dashboard and start adding Departments and Employees.

---

📝 Assumptions & Logic Decisions

*   Calculations: Gross Pay is calculated as `Basic Salary + Allowance + (Overtime Hours * Hourly Rate)`.

*   PDF Exports: Payslips are generated as PDF files using the `dompdf` library for professional printing.

---
