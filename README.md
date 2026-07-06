<div align="center">

# 🛒 OpenCart (Frontend) — Manual QA Testing Project

**End-to-end functional testing of the OpenCart e-commerce demo store**
`https://demo.opencart.com/`

[![Test Cases](https://img.shields.io/badge/Test%20Cases-516-blue)]()
[![Pass Rate](https://img.shields.io/badge/Pass%20Rate-89%25-brightgreen)]()
[![Bugs Logged](https://img.shields.io/badge/Defects%20Logged-23-red)]()

</div>

---

## 📖 Overview

This repository documents a complete **manual QA testing cycle** on the OpenCart storefront — from requirement analysis and test planning, through test design and execution, to defect reporting and traceability. It's a portfolio project simulating a real-world QA engagement on a live, public demo application.

| | |
|---|---|
| **Application Under Test** | [demo.opencart.com](https://demo.opencart.com/) |
| **Module Tested** | OpenCart Storefront (customer-facing frontend) |
| **Testing Type** | Manual Functional Testing |
| **Prepared By** | Shivam Patidar |

---

## 📂 What's in This Repo

| Document | File | What it covers |
|---|---|---|
| Functional Requirements | `OpenCart_-FRS.pdf` | Intended behavior of the storefront (nav, product pages, cart, checkout) |
| Test Plan | `OpenCart_-Test_Plan.pdf` | Scope, strategy, schedule, roles, entry/exit criteria |
| Test Scenarios | `OpenCart-Test_Scenarios_.xlsx` | 31 high-level scenarios, one per functional area |
| Test Cases | `OpenCart-TestCases.xlsx` | 516 step-by-step test cases across 31 modules |
| Test Execution Results | `OpenCart-TestExecution_Results.xlsx` | Pass/Fail/Blocked status + linked defects, per test case |
| Bug Report | `OpenCart-BugReport.xlsx` | 23 logged defects with repro steps and screenshots |
| RTM | `OpenCart-RTM.xlsx` | Requirement → Scenario → Test Case traceability |

> Start with the FRS (what it should do) → Test Plan (how it was tested) → Execution Results & Bug Report (what was found).

---

## 🎯 Scope

**In scope:** Register, Login/Logout, Forgot Password, Search, Product Compare, Product Display Page, Add to Cart, Wish List, Shopping Cart, Currencies, Home Page, Checkout, My Account, Order History, Downloads, Contact Us, Menu/Footer Options, Category Pages

**Out of scope:** Payment gateways & third-party integrations, test automation, OpenCart admin/backend

**Environments:** Windows 10 (Chrome, Firefox, Edge) · macOS (Safari) · Android (Chrome) · iOS (Safari)

---

## 🧪 Methodology

- **Test design:** Equivalence Partitioning, Boundary Value Analysis, Decision Tables, State Transition & Use Case testing, plus Error Guessing and Exploratory Testing
- **Execution flow:** Smoke test → reject unstable builds → full functional pass → regression/retest after fixes
- **Practices:** Shift-left testing, context-driven testing, end-to-end user-flow validation (e.g. Register → Search → Cart → Checkout)
- **Defect lifecycle:** every deviation logged with screenshots + repro steps, retested for reproducibility, summarized daily

---

## 📊 Results at a Glance

**516** test cases designed · **514** executed · **23** defects logged

| Result | Count | % |
|---|:---:|:---:|
| ✅ Pass | 458 | 89% |
| ❌ Fail | 25 | 5% |
| 🚫 Blocked | 31 | 6% |

| Defect Severity | Critical | Major | Minor |
|---|:---:|:---:|:---:|
| Count | 4 | 7 | 12 |

Blocked cases were concentrated mainly in **Forgot Password** and **Gift Certificate**, largely due to email-delivery dependencies in the demo environment.

📄 *Full module-by-module breakdown is in `OpenCart-TestExecution_Results.xlsx`.*

---

## 🐞 Notable Defects

| Bug ID | Summary | Severity |
|---|---|:---:|
| OPENCART-BUG-20 | Product option dropdown shows no selectable values (Canon EOS 5D) | Critical |
| OPENCART-BUG-19 | Non-affiliate users can log in via the Affiliate Login section | Critical |
| OPENCART-BUG-17 | Future dates accepted for Order Return date | Critical |
| OPENCART-BUG-7 | User gets logged out when clicking browser Back button | Critical |
| OPENCART-BUG-5 | Weak/simple passwords accepted — no complexity check | Major |
| OPENCART-BUG-1 | Registration confirmation email not received | Major |

📄 *All 23 defects — with steps to reproduce, expected vs. actual results, and screenshots — are in `OpenCart-BugReport.xlsx`.*

---

## 🛠 Tools

Excel (test scenarios, test cases, execution tracking, bug tracking) · Snipping Tool (screenshots) · Mind mapping (test idea generation)

---

## 🌟 Key Highlights

- Designed 31 scenarios and 516 test cases from a single FRS document using multiple test-design techniques
- ~89% first-cycle pass rate across 31 functional modules
- Found 4 Critical / 7 Major defects affecting session handling, registration validation, and product options
- Maintained full requirement-to-test-case traceability via RTM

---

## 👤 Author

**Shivam Patidar** — QA / Software Test Engineer

*Portfolio project using the public OpenCart demo store (`https://demo.opencart.com/`) as the application under test.*
