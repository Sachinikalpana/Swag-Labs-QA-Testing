# Swag Labs (SauceDemo) - Manual QA Testing & Jira Defect Tracking

## 📌 Project Overview
This repository contains the manual QA test suite and execution results for the **Swag Labs (SauceDemo)** e-commerce application. The project demonstrates end-to-end quality assurance workflows, including test design in Excel and defect tracking in **Jira Software (Kanban Workflow)**.

* **Target Application:** [SauceDemo Web App](https://www.saucedemo.com)
* **QA Lead:** Sachini
* **Execution Date:** August 6, 2026
* **Test Management Tool:** Microsoft Excel
* **Defect Tracking Tool:** Jira Software
* **Tested Environment:** Google Chrome / Windows 11

---

## 📊 Test Execution Summary

| Metric | Details |
| :--- | :--- |
| **Total Test Cases Executed** | 13 |
| **Passed** | 12 |
| **Failed** | 1 |
| **Pass Rate** | 92.3% |
| **Critical Defect Logged** | 1 (`SLQ-4`) |

---

## 🛠️ Test Suite Breakdown

### 1. Login Interface (`TS_01`) — 7 Test Cases
* `TS_01_TC_01`: Valid username and password authentication **(Pass)**
* `TS_01_TC_02`: Valid username with invalid password validation **(Pass)**
* `TS_01_TC_03`: Invalid username with valid password validation **(Pass)**
* `TS_01_TC_04`: Invalid username with invalid password validation **(Pass)**
* `TS_01_TC_05`: Empty credentials validation **(Pass)**
* `TS_01_TC_06`: Locked-out user prevention handling **(Pass)**
* `TS_01_TC_07`: Application logout via side navigation menu **(Pass)**

### 2. Product Catalog & Shopping Cart (`TS_02`) — 4 Test Cases
* `TS_02_TC_01`: Verify item details and image rendering for `standard_user` **(Pass)**
* `TS_02_TC_02`: Verify product sorting logic (Price low to high) **(Pass)**
* `TS_02_TC_03`: Verify adding item to shopping cart & badge update **(Pass)**
* `TS_02_TC_04`: Verify product image rendering for `problem_user` **(Fail — Logged as Jira `SLQ-4`)**

### 3. Checkout Flow (`TS_03`) — 2 Test Cases
* `TS_03_TC_01`: Verify successful end-to-end checkout **(Pass)**
* `TS_03_TC_02`: Verify mandatory field validation (Blank First Name) **(Pass)**

---

## 🐞 Logged Defect Summary

### Bug Ticket: `SLQ-4`
* **Summary:** `[Catalog] Broken product image rendering on inventory page for problem_user`
* **Severity / Priority:** High
* **Status:** In Progress
* **Steps to Reproduce:**
  1. Navigate to `https://www.saucedemo.com`
  2. Log in using `problem_user` and `secret_sauce`
  3. Inspect product images on `/inventory.html`
* **Expected Result:** Every product displays its unique, high-resolution product photo.
* **Actual Result:** All product cards display the exact same broken fallback dog picture.

---

## 📁 Repository Contents
* `Swag_Labs_Test_Cases.xlsx` — Full 13-case Excel test execution suite.
* `README.md` — Project documentation and QA execution report.
* `screenshots/` — Visual proof of Jira board, Excel sheet, and bug reproduction.
