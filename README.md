# 🏦 Banking Application – Manual Testing

> **Manual Testing | Test Cases | Bug Reports | SQL Validation**  
> Tested by **Swapnil Kamble** | QA Engineer

---

## 📌 Project Overview

This repository contains complete manual testing documentation for a Banking Web Application.
It covers test planning, test case design, execution, defect reporting, and database validation
for all core banking modules.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Microsoft Excel | Test cases & bug reports |
| JIRA | Defect tracking & management |
| SQL | Backend / database validation |
| Manual Testing | Functional, Regression, BVT, Smoke |

---

## 📁 Repository Structure

```
banking-manual-testing/
├── Test-Cases/
│   └── Banking_Manual_Testing.xlsx    # All 20+ test cases
│       ├── Sheet 1 - Test Cases       # Detailed test cases per module
│       ├── Sheet 2 - Bug Reports      # 7 defects with severity/priority
│       └── Sheet 3 - Test Summary     # Module-wise pass/fail summary
├── README.md
```

---

## ✅ Modules Tested

### 🔐 Login Module (5 Test Cases)
- Valid login with correct credentials
- Invalid password error handling
- Empty email/password validation
- Invalid email format validation

### 🏦 Account Management (5 Test Cases)
- Create new bank account
- View account balance
- Edit customer details
- Delete account
- Search non-existent account

### 💸 Fund Transfer (5 Test Cases)
- Successful fund transfer between accounts
- Transfer with insufficient balance
- Transfer to invalid account
- Zero amount transfer validation
- Negative amount transfer validation

### 📊 Reports (3 Test Cases)
- Generate transaction report by date range
- Invalid date range validation
- Export report to CSV

### 🗄️ Database Validation (2 Test Cases)
- Verify balance after fund transfer via SQL
- Verify new account record in database via SQL

---

## 🐛 Bug Summary

| Bug ID | Module | Severity | Status |
|---|---|---|---|
| BUG_001 | Login | High | Fixed |
| BUG_002 | Account Mgmt | Critical | Fixed |
| BUG_003 | Fund Transfer | Critical | Fixed |
| BUG_004 | Reports | Low | Fixed |
| BUG_005 | Login | Medium | Fixed |
| BUG_006 | Fund Transfer | Medium | Open |
| BUG_007 | Reports | High | Open |

**Total: 7 bugs found | 5 Fixed | 2 Open**

---

## 📊 Test Execution Summary

| Module | Total | Passed | Failed | Pass % |
|---|---|---|---|---|
| Login | 5 | 5 | 0 | 100% |
| Account Management | 5 | 5 | 0 | 100% |
| Fund Transfer | 5 | 5 | 0 | 100% |
| Reports | 3 | 3 | 0 | 100% |
| Database Validation | 2 | 2 | 0 | 100% |
| **TOTAL** | **20** | **20** | **0** | **100%** |

---

## 🗄️ Sample SQL Queries Used

```sql
-- Verify balance after fund transfer
SELECT account_id, balance FROM accounts WHERE account_id = 10001;

-- Verify new account creation
SELECT * FROM accounts WHERE customer_name = 'Rahul Sharma';

-- Check transaction history
SELECT * FROM transactions WHERE from_account = 10001 ORDER BY txn_date DESC;
```

---

## 👤 Author

**Swapnil Kamble**  
QA Engineer | Solapur, Maharashtra  
🎓 Udemy Certified – Software Manual Testing (March 2026)
