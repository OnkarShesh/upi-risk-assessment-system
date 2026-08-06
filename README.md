# UPI Risk Assessment System

A rule-based UPI transaction risk assessment system that analyzes transactions in real time and assigns a risk score based on suspicious activity patterns. Developed using **Node.js**, **Express.js**, and **JavaScript** during the **Fiserv Hackathon**.

---

## Overview

The application evaluates UPI transactions using predefined risk assessment rules and classifies each transaction as **Low**, **Medium**, or **High Risk**. It also provides transaction monitoring, user risk profiling, and suspicious transaction export.

---

## Features

- Real-time UPI transaction risk assessment
- Rule-based fraud detection engine
- Dynamic risk score calculation
- Low, Medium, and High risk classification
- High-value transaction detection
- High transaction velocity detection
- New beneficiary detection
- Device change detection
- Unusual transaction timing detection
- User risk profile dashboard
- Transaction monitoring dashboard
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
upi-risk-assessment-system/
├── public/
│   └── index.html
├── server.js
├── ruleEngine.js
├── package.json
├── package-lock.json
├── README.md
└── .gitignore
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/OnkarShesh/upi-risk-assessment-system.git
```

Navigate to the project directory

```bash
cd upi-risk-assessment-system
```

Install dependencies

```bash
npm install
```

Start the application

```bash
npm start
```

Open your browser

```
http://localhost:3000
```

---

## API Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | `/api/transaction` | Analyze a transaction |
| GET | `/api/transactions` | Retrieve all transactions |
| GET | `/api/transactions?filter=flagged` | Retrieve flagged transactions |
| GET | `/api/profile/:userId` | Get user risk profile |
| POST | `/api/burst` | Generate sample transactions |
| GET | `/api/export` | Export suspicious transactions as CSV |

---

## Sample Request

```json
{
  "payer_id": "user_001",
  "payee_id": "merchant_42",
  "amount": 15000,
  "location": "Mumbai",
  "device_id": "dev_abc123",
  "hour_override": 3
}
```

---

## Risk Assessment Rules

The transaction risk score is calculated using multiple rule-based checks, including:

- High-value transactions within a short time window
- New beneficiary with a high transaction amount
- High transaction velocity
- Transactions during unusual hours (12 AM – 5 AM)
- Device change combined with a new beneficiary
- Large transaction amount

Each triggered rule contributes to the overall risk score.

---

## Risk Classification

| Score | Risk Level |
|-------:|------------|
| 0 – 29 | Low |
| 30 – 59 | Medium |
| 60 – 100 | High |

---

## Testing Scenarios

The system can be tested using scenarios such as:

- High-value transactions
- Multiple rapid transactions
- New beneficiary payments
- Device change
- Transactions during unusual hours
- Burst transaction simulation

---

## Screenshots

### Dashboard

> Add `screenshots/dashboard.png`

### User Risk Profile

> Add `screenshots/user-risk-profile.png`

### CSV Export

> Add `screenshots/csv-export.png`

---

## Future Improvements

- Machine Learning based fraud detection
- Database integration (MongoDB/PostgreSQL)
- JWT Authentication
- Redis caching
- Real-time analytics
- Docker deployment

---

## Developed During

**Fiserv Hackathon**

---

## Author

**Onkar Shesh**

GitHub: https://github.com/OnkarShesh