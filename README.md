# 💼 HR Management System – Manual Testing Project

This is a **realistic manual testing project** built to simulate testing of an end-to-end Human Resource Management System (HRMS). It covers test case design, bug reporting, and backend (SQL) validation for common HR modules like onboarding, leave, payroll, and appraisals.

This project showcases hands-on experience with manual test design, exploratory testing, SQL query-based DB validation, and defect management using best industry practices.

---

## 🧪 Project Type: Manual Testing (Real-World Simulation)

---

## 📚 Table of Contents
- [Project Overview](#project-overview)
- [Modules Covered](#modules-covered)
- [Test Artifacts](#test-artifacts)
- [Tools & Technologies](#tools--technologies)
- [Test Case Summary](#test-case-summary)
- [Bug Report Summary](#bug-report-summary)
- [SQL Testing Examples](#sql-testing-examples)
- [Folder Structure](#folder-structure)
- [Author](#author)

---

## 📝 Project Overview

**HR Management System (HRMS)** is used to manage employee onboarding, leave tracking, payroll processing, and performance appraisals. It is used by HR teams, employees, and management.

This project simulates manual testing lifecycle from test case writing → execution → bug reporting → backend validation using SQL queries.

---

## 📦 Modules Covered

| Module             | Description |
|--------------------|-------------|
| **Employee Onboarding** | Add/edit employee records with validation |
| **Leave Management**     | Apply, approve/reject leaves, check balance |
| **Payroll**              | Generate salary slip, validate calculations |
| **Appraisal**            | Submit/view employee performance ratings |
| **Login & Profile**      | Auth, edit profile, security testing |
| **UI/UX + Browser**      | Responsive layout, cross-browser compatibility |
| **Database Testing**     | Query verification post-action |

---

## 📂 Test Artifacts

This project contains the following:

| File | Description |
|------|-------------|
| `HRMS_TestCases.xlsx` | 30 manual test cases with steps, expected & actual results |
| `HRMS_Bug_Report_Sample.xlsx` | 8 realistic bug reports with severity & priority |
| `HRMS_SQL_Testing_Queries.txt` | SQL queries to validate backend operations |
| `README.md` | Project summary and documentation |

---

## 🛠️ Tools & Technologies

- ✅ **Excel** – Test case documentation and bug reports
- ✅ **MySQL / SQL** – Backend data validation
- ✅ **JIRA Format** – Sample bug reports (manual)
- ✅ **Windows 11** – Test environment
- ✅ **Browsers** – Chrome, Firefox, Edge, IE
- ✅ **Agile** – Sprint-based testing process

---

## ✅ Test Case Summary

| Total Test Cases | Status | Coverage |
|------------------|--------|----------|
| 30               | Pass/Fail (manual) | Onboarding, Leave, Payroll, Appraisal, UI, DB |

Test cases include both **positive** and **negative scenarios**, covering edge cases and business logic validation.

---

## 🐞 Bug Report Summary

| Total Bugs | Status | Severity Breakdown | Priority |
|------------|--------|--------------------|----------|
| 8         | Open (sample) | Critical: 1, High: 4, Medium: 2, Low: 1 | Urgent, High, Medium, Low |

Defects logged include functional issues, UI glitches, validation errors, business logic failures, and database mismatches.

---

## 🧾 SQL Testing Examples

Sample SQL queries from the project:

```sql
-- Verify employee added correctly
SELECT * FROM employees WHERE employee_id = 1001;

-- Leave balance updated after approval
SELECT leave_balance FROM leave_records WHERE employee_id = 1001;

-- Validate payroll generation
SELECT * FROM payroll WHERE employee_id = 1001 AND month = '2024-03';

-- Appraisal history check
SELECT * FROM appraisals WHERE employee_id = 1001;

-- Join example: show employee with approved leaves
SELECT e.name, l.leave_type 
FROM employees e 
JOIN leave_requests l ON e.employee_id = l.employee_id 
WHERE l.status = 'Approved';
