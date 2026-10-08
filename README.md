# VYOM+ — Intelligent Voucher Classification

> An open-source AI-powered accounting intelligence engine that understands structured financial transactions and automatically determines the appropriate accounting voucher category.

---

## 1. Project Name

# VYOM+ Intelligent Voucher Classification

### Tagline

**From Transaction Data to Accounting Intelligence.**

VYOM+ is an AI-powered voucher classification system that analyses structured transaction information and predicts the appropriate accounting voucher category using an open-source Large Language Model (LLM), structured reasoning, validation rules and contextual transaction analysis.

---

## 2. Problem Statement

Modern accounting systems process large volumes of financial transactions such as purchases, sales, payments, receipts, returns, stock movements, payroll, imports and exports.

Although the transaction data may already be structured, determining the correct accounting voucher type still requires understanding the relationship between multiple fields.

For example, the distinction between:

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

The challenge is therefore to build an intelligent system that understands the complete transaction context and predicts the most appropriate voucher category.

The input dataset contains structured transaction information while the voucher-type field is intentionally missing.

---

## 3. Project Overview

VYOM+ acts as an intelligent classification layer between structured transaction data and automated accounting workflows.

The system accepts an Excel dataset containing transaction records and analyses multiple fields including:

- Supplier / Seller
- Buyer / Customer
- Invoice information
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

The system then:

1. Reads the transaction dataset.
2. Normalises and validates the input.
3. Builds a contextual representation of each transaction.
4. Analyses accounting signals.
5. Uses an open-source LLM as the primary intelligence layer.
6. Generates a structured voucher prediction.
7. Assigns a confidence score.
8. Produces supporting reasoning/evidence.
9. Validates the prediction.
10. Exports machine-readable results.

---

## 4. Proposed Solution

We propose a **Hybrid AI Voucher Classification Engine** combining:

- Structured transaction preprocessing
- Accounting-aware feature extraction
- Rule-based validation
- Semantic representation
- Open-source LLM classification
- Confidence estimation
- Structured output validation
- Explainable classification

### High-Level Workflow

```mermaid
flowchart LR

A[Excel Transaction Dataset]
--> B[Data Ingestion]

B --> C[Validation & Normalisation]

C --> D[Transaction Context Builder]

D --> E[Accounting Signal Extraction]

E --> F[Open-Source LLM]

F --> G[Candidate Voucher Classification]

G --> H[Rule & Consistency Validator]

H --> I[Confidence Scoring]

I --> J[Explanation Generator]

J --> K[Structured Output]

K --> L[Dashboard / Excel / JSON]