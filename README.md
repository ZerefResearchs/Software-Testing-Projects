
# Omnify QA Assignment – Manual Testing (OrangeHRM)

This repository contains the **manual testing deliverables** for the Omnify QA Assignment.  
System under test: **OrangeHRM Demo** — [https://opensource-demo.orangehrmlive.com](https://opensource-demo.orangehrmlive.com)

---

## 📖 Table of Contents
1. [Project Scope](#project-scope)  
2. [Test Data](#test-data)  
3. [Sheet 1 — Login Test Cases](#sheet-1--login-test-cases)  
4. [Sheet 2 — PIM (Employee Management) Test Cases](#sheet-2--pim-employee-management-test-cases)  
5. [Sheet 3 — Bug Report (includes 3 login issues)](#sheet-3--bug-report-includes-3-login-issues)  
6. [Sheet 4 — Test Execution Summary](#sheet-4--test-execution-summary)  
7. [Screenshots & Evidence](#screenshots--evidence)  


---

## 📌 Project Scope
- **Login functionality** — positive, negative and edge cases.  
- **PIM (Employee Management):**  
  - Add Employee  
  - Search/View Employee  
  - Edit Employee  
  - Delete Employee  
  - Search/Reset  
  - Pagination  

Deliverables include:
- Test Cases (Login + PIM)  
- Bug Report (with 3 login issues)  
- Test Execution Summary  
- Screenshots as test evidence  

---

## 📊 Test Data
We used sample employee records stored in `testdata_employees.csv` format:



---

## 📑 Sheet 1 — Login Test Cases

| Test Case ID | Title              | Steps (detailed)                                                                 | Expected Result                                 | Status | Screenshot |
|--------------|-------------------|----------------------------------------------------------------------------------|-------------------------------------------------|--------|------------|
| LOGIN-01     | Valid login        | 1. Open login page. 2. Enter `Admin` / `admin123`. 3. Click **Login**. | User is redirected to Dashboard; Admin profile visible. | Pass | [View](./screenshots/Login-Test-Cases/Login-01.png) |
| LOGIN-02     | Invalid password   | 1. Enter `Admin` and invalid password. 2. Click **Login**. | Error message displayed: “Invalid credentials”. | Pass | [View](./screenshots/Login-Test-Cases/Login-02.png) |
| LOGIN-03     | Invalid username   | 1. Enter invalid username and valid password. 2. Click **Login**. | Error message displayed: “Invalid credentials”. | Pass | [View](./screenshots/Login-Test-Cases/Login-03.png) |
| LOGIN-04     | Empty fields       | 1. Leave username and/or password blank. 2. Click **Login**. | Required field error messages displayed. | Pass | [View](./screenshots/Login-Test-Cases/Login-04.png) |
| LOGIN-05     | SQL / special char input | 1. Enter `' OR '1'='1` in username field. 2. Click **Login**. | System does not allow login; error shown. | Pass | [View](./screenshots/Login-Test-Cases/Login-05.png) |
| LOGIN-06     | Password masking   | 1. Type into password field. | Input characters masked (dots/bullets). | Pass | [View](./Screenshots/Login-Test-Cases/Login-06.png) |
| LOGIN-07     | Session / logout behavior | 1. Login. 2. Logout. 3. Press browser Back button. | Protected pages not accessible; redirected to login. | Fail | [View](./screenshots/Login-Test-Cases/Login-07.png) |
| LOGIN-08     | Error clarity      | 1. Enter invalid credentials. 2. Observe error. | Error message should be clear, readable and accessible. | Fail | [View](./screenshots/Login-Test-Cases/Login-08.png) |

---

## 📑 Sheet 2 — PIM (Employee Management) Test Cases

| Test Case ID | Title            | Steps (detailed)                                                                 | Expected Result                          | Status | Screenshot |
|--------------|-----------------|----------------------------------------------------------------------------------|------------------------------------------|--------|------------|
| PIM-01       | Add Employee     | Login → PIM → Employee List → Add → Fill form with CSV data → Save. | New employee created successfully. | Pass | [View](./screenshots/PIM-Test-Cases/PIM-01.png) |
| PIM-02       | Search Employee  | PIM → Employee List → Search by Name/ID. | Matching employee record displayed. | Pass | [View](./screenshots/PIM-Test-Cases/PIM-02.png) |
| PIM-03       | Edit Employee    | Search employee → Edit → Update Last Name → Save. | Updated details visible in Employee List. | Pass | [View](./screenshots/PIM-Test-Cases/PIM-03.png) |
| PIM-04       | Delete Employee  | Search employee → Delete → Confirm. | Employee removed from Employee List. | Pass | [View](./screenshots/PIM-Test-Cases/PIM-04.png) |
| PIM-05       | Pagination       | PIM → Employee List → Navigate Next/Prev. | Pagination works and updates rows. | Pass | [View](./screenshots/PIM-Test-Cases/PIM-05.png) |
| PIM-06       | Reset Search     | Enter criteria → Search → Click Reset. | Filters clear and full list displayed. | Pass | [View](./screenshots/PIM-Test-Cases/PIM-06.png) |

---

## 📑 Sheet 3 — Bug Report (includes 3 login issues)

### Potential Bugs & Usability Issues (Login Page)

| Bug ID       | Module | Title / Description | Steps to Reproduce | Expected Result | Severity | Screenshot |
|--------------|--------|---------------------|--------------------|-----------------|----------|------------|
| BUG-LOGIN-01 | Login  | Ambiguous error message | 1. Enter valid username + invalid password. <br> 2. Click **Login**. | Error message should clearly state “Invalid username or password” without ambiguity. | Medium | [View](./screenshots/Bug-Report/BUG-LOGIN-01.png) |
| BUG-LOGIN-02 | Login  | Login button allows duplicate clicks | 1. Enter credentials. <br> 2. Double-click **Login** rapidly. | Login button should disable after first click to prevent duplicate submissions. | Medium | [View](./screenshots/Bug-Report/BUG-LOGIN-01.png) |
| BUG-LOGIN-03 | Login  | Username case sensitivity issue | 1. Enter Admin → Login successful. 2. Enter admin (all lowercase) → Login also successful. | System should enforce case sensitivity (if requirement is strict) OR document that it’s case-insensitive. | Low | [View](./screenshots/Bug-Report/BUG-LOGIN-01.png) |



---

## 📑 Sheet 4 — Test Execution Summary

| Module | Total Test Cases | Passed | Failed | Blocked/Skipped | Execution Date | Tester |
|--------|------------------|--------|--------|-----------------|----------------|--------|
| Login  | 8                | 6    | 2    | 0             | 02-OCT-2025     | Munendra Pal |
| PIM    | 6                | 6    | 0    | 0             | 02-OCT-2025     | Munendra Pal |
| **Total** | 14             | 12    | 2    | 0             | 02-OCT-2025     | Munendra Pal |



---

## 📸 Screenshots & Evidence
- All screenshots stored in: [Manual/Screenshots/](./Manual/Screenshots)  
- Linked in the **Screenshot** column of each test case and bug.  
- Naming convention:  
  - `LOGIN-01.png` → Valid login test  
  - `PIM-01.png` → Add employee test  
  - `BUG-LOGIN-01.png` → Bug evidence for login page  




---

👨‍💻 **Author:** Munendra Pal  
📅 **Submission Date:** 02-OCT-2025  
🔗 **GitHub Repo Link:** [repo link](https://github.com/MUNENDRA10/Omnify-OrangeHRM-Manual-Testing-Assignment)
