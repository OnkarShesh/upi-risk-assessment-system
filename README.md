# UPI Risk Assessment System

A rule-based UPI transaction risk assessment system that analyzes transactions in real time and assigns a risk score based on suspicious activity patterns. Developed during the **Fiserv Hackathon** using **Node.js** and **Express.js**.

---

## Overview

The system evaluates every UPI transaction against predefined fraud detection rules and classifies it as **Low**, **Medium**, or **High Risk**. It demonstrates how financial institutions can perform instant transaction risk analysis before processing payments.

---

## Features

- Real-time transaction risk assessment
- Rule-based fraud detection engine
- Dynamic risk score calculation
- Low / Medium / High risk classification
- New beneficiary detection
- Device change detection
- High-value transaction detection
- Night-time transaction monitoring
- High transaction velocity detection
- User transaction profiling
- Transaction history dashboard
- CSV export for suspicious transactions

---

## Tech Stack

**Frontend**
- HTML
- CSS
- JavaScript

**Backend**
- Node.js
- Express.js

---

## Project Structure

```
upi-risk-assessment-system
│
├── public/
│   └── index.html
│
├── server.js
├── ruleEngine.js
├── package.json
├── package-lock.json
└── README.md
```

---

## Fraud Detection Rules

The risk engine evaluates transactions using multiple rules including:

- High-value transactions
- Multiple transactions within a short time
- New beneficiary detection
- Device change detection
- Unusual transaction timing (12 AM – 5 AM)
- Large transaction amount

Each triggered rule contributes to the overall risk score.

---

## Risk Levels

| Score | Risk Level |
|-------:|------------|
| 0 – 29 | Low |
| 30 – 59 | Medium |
| 60 – 100 | High |

---

## System Workflow

```
User Transaction
        │
        ▼
Express Server
        │
        ▼
Rule Engine
        │
        ▼
Risk Score Calculation
        │
        ▼
Low / Medium / High
        │
        ▼
Dashboard & Transaction History
```

---

## API Endpoints

### Analyze Transaction

```
POST /api/transaction
```

### Get User Profile

```
GET /api/profile/:userId
```

### Generate Sample Transactions

```
POST /api/burst
```

### Export Suspicious Transactions

```
GET /api/export
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/OnkarShesh/upi-risk-assessment-system.git
```

Go to the project directory

```bash
cd upi-risk-assessment-system
```

Install dependencies

```bash
npm install
```

Start the server

```bash
npm start
```

Open

```
http://localhost:3000
```

---

## Future Improvements

- Machine Learning based fraud detection
- MongoDB/PostgreSQL integration
- JWT Authentication
- Redis caching
- Real-time analytics dashboard
- Email/SMS alerts
- Docker deployment

---

## Hackathon

Developed during the **Fiserv Hackathon** as a prototype demonstrating real-time UPI transaction risk assessment using a rule-based approach.

---

## Author

**Onkar Shesh**

GitHub: https://github.com/OnkarShesh
