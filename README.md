# README

# 🛠️ Toolshop - Manual QA Testing Project

## 📋 Project Overview

This repository documents a full manual QA testing cycle performed on [**Practice Software Testing (Toolshop)**](https://practicesoftwaretesting.com/) — an e-commerce demo application built for QA practice, tested here via its `with-bugs` version.

The project covers the **complete checkout journey end-to-end**: from selecting a product, through the cart, login, address, and payment steps — with full test case design, execution, and defect reporting.

## 🎯 Objectives

- Design and execute test cases covering functional, negative, boundary, and security scenarios
- Identify and document real, reproducible bugs across the checkout flow
- Apply structured test design techniques (Equivalence Partitioning, Boundary Value Analysis)
- Practice end-to-end manual QA documentation: Test Cases, Bug Reports, Test Summary Report

## 🧪 Areas Tested

- Quantity Selector (product page)
- Add to Cart
- Cart Page (item totals, cart total, item removal)
- Login & Authentication (including security testing)
- Address / Checkout Step
- Payment

## 📊 Test Execution Summary

| Metric | Count |
| --- | --- |
| Total Test Cases | 59 |
| Passed | 38 |
| Failed | 21 |
| Pass Rate | 64.4% |

## 🐞 Bug Summary

| Severity | Count | Percentage |
| --- | --- | --- |
| High | 6 | 29% |
| Medium | 6 | 29% |
| Low | 9 | 42% |
| **Total** | **21** | **100%** |

### Bugs by Feature

| Feature | Bug Count |
| --- | --- |
| Quantity Selector | 3 |
| Add to Cart | 2 |
| Cart Page | 4 |
| Login | 0 |
| Address | 4 |
| Payment | 8 |

## 🚨 Most Critical Issues Found

1. **Item total always displays $00.00** on the Cart page, regardless of price or quantity — while the overall cart total calculates correctly. This points to a display-layer bug rather than a backend calculation issue.
2. **A successful “Add to Cart” action shows an error toast** (“Oops, something went wrong”) even though the product is added correctly — a misleading message that could confuse real users.
3. **Quantity Plus/Minus buttons do not respond**, and manually typed quantities are appended rather than replacing the existing value.
4. **Address fields arrive pre-filled with unrelated placeholder data** (including the literal text “missing value”) instead of being empty.
5. **An internal error message** (“Error 304 - Missing Payment Gateway”) appears as a **selectable option** in the Payment method dropdown.

## ✅ What Worked Well

- Login page correctly rejected **XSS** and **SQL Injection** attempts on the email field
- Cart total (the overall order total) calculated correctly even when the per-item total did not
- Core navigation and page-to-page checkout flow (Cart → Sign In → Address → Payment) worked as expected

## 🛠️ Testing Approach

**Methodology:** Scripted manual testing with structured test case design, combined with light exploratory testing while executing.

**Techniques used:**
- Equivalence Partitioning (valid/invalid input classes)
- Boundary Value Analysis (min/max lengths, quantity limits)
- Negative Testing (invalid inputs, empty fields)
- Basic Security Testing (XSS, SQL Injection)
- UI / Navigation Testing

## 📁 Repository Contents

| File | Description |
| --- | --- |
| `Toolshop_Manual_Testing_Project.xlsx` | Full test summary, test cases (59 TCs), and bug reports (21 bugs) |

## 🎯 Skills Demonstrated

- Test Case Design (Equivalence Partitioning, Boundary Value Analysis)
- Manual Functional & Regression Testing
- Security Testing Fundamentals (XSS, SQL Injection)
- Defect Reporting & Severity Classification
- End-to-End Checkout Flow Validation

---

**Tester:** Mohab Elhosseny
**Environment:** Web - Chrome | [with-bugs.practicesoftwaretesting.com](https://with-bugs.practicesoftwaretesting.com/)