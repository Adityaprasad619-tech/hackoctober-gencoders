# VYOM+ — Intelligent Voucher Classification

> **From Transaction Data to Accounting Intelligence**

An open-source AI-powered accounting intelligence system that understands structured financial transactions and automatically determines the appropriate accounting voucher category.

---

## 1. Project Name

# VYOM+ Intelligent Voucher Classification

### Tagline

**From Transaction Data to Accounting Intelligence.**

VYOM+ is an AI-powered voucher classification system that analyses structured transaction information and predicts the appropriate accounting voucher category using an open-source Large Language Model (LLM), accounting-aware reasoning, validation rules, confidence scoring, and explainable classification.

---

## 2. Problem Statement

Modern accounting systems process large volumes of financial transactions such as purchases, sales, payments, receipts, returns, stock movements, payroll, imports, and exports.

Although transaction data may already be structured, determining the correct accounting voucher type requires understanding the relationship between multiple fields.

For example, distinguishing between:

- Purchase vs Sales
- Purchase Return vs Sales Return
- Payment vs Receipt
- Contra vs Payment/Receipt
- Journal vs conventional transactions
- Material In vs Purchase
- Material Out vs Sales
- Import vs Purchase
- Export vs Sales

cannot reliably be determined from a single keyword.

The challenge is therefore to build an intelligent system that understands the **complete transaction context** and predicts the most appropriate voucher category.

The input dataset contains structured transaction information while the voucher-type field is intentionally missing.

---

## 3. Project Overview

VYOM+ acts as an intelligent classification layer between structured transaction data and automated accounting workflows.

The system accepts an Excel dataset containing transaction records and analyses multiple fields including:

- Seller / Supplier
- Buyer / Customer
- Invoice number and date
- Item descriptions
- Quantity
- Taxable value
- GST
- Discounts
- Freight
- Payment information
- Currency
- Import / Export information
- Payroll information
- Debit / Credit information
- Return information
- Order references
- Delivery information
- Other transaction metadata

### Core Process

1. Read the transaction dataset.
2. Validate and normalise the input.
3. Build a contextual representation of each transaction.
4. Extract accounting-relevant signals.
5. Analyse the transaction using an open-source LLM.
6. Predict the appropriate voucher category.
7. Validate the prediction.
8. Calculate a confidence score.
9. Generate supporting evidence.
10. Produce structured machine-readable output.

---

## 4. Proposed Solution

We propose a **Hybrid AI Voucher Classification Engine** combining:

- Structured transaction preprocessing
- Accounting-aware signal extraction
- Rule-based validation
- Semantic transaction representation
- Open-source LLM reasoning
- Confidence estimation
- Structured output validation
- Explainable classification

### High-Level Solution

```mermaid
flowchart LR
    A["Excel Transaction Dataset"] --> B["Data Ingestion"]
    B --> C["Validation & Normalisation"]
    C --> D["Transaction Context Builder"]
    D --> E["Accounting Signal Extraction"]
    E --> F["Open-Source LLM"]
    F --> G["Voucher Classification"]
    G --> H["Rule & Consistency Validation"]
    H --> I["Confidence Scoring"]
    I --> J["Explanation & Evidence"]
    J --> K["Structured Output"]
    K --> L["Dashboard / JSON / Excel"]