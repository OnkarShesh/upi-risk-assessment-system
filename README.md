UPI Fraud Detection System

This is a small project I made to detect fraud in UPI transactions.
It uses simple rule-based logic to check if a transaction looks suspicious or not.

I built it using Node.js and Express, and a basic HTML page for frontend.
There is no database — everything runs in memory.

Folder Structure
upi-fraud-detector/
├── server.js          (main backend file)
├── ruleEngine.js      (fraud rules logic)
├── package.json
├── README.md
└── public/
    └── index.html     (simple UI)
How to Run

Make sure Node.js is installed.

Then run:

cd upi-fraud-detector
npm install
npm start

Open browser:
http://localhost:3000

APIs
POST /api/transaction → add transaction
GET /api/transactions → get all
GET /api/transactions?filter=flagged → only suspicious
GET /api/profile/:userId → user data
POST /api/burst → test multiple transactions
GET /api/export → download CSV

Example:

{
  "payer_id": "user_001",
  "payee_id": "merchant_42",
  "amount": 15000,
  "location": "Mumbai",
  "device_id": "dev_abc123",
  "hour_override": 3
}
How Fraud Detection Works

There are some basic rules like:

high amount transactions in short time
new merchant with high amount
too many transactions quickly
transactions at odd hours
new device + new payee

Each rule adds some score.
Based on total score:

Low → 0–29
Medium → 30–59
High → 60–100
Testing

You can try:

set time to 2 AM
use new payee + high amount
change device id
use burst option
send 2 big transactions quickly
Features
simple rule-based fraud detection
shows risk level
user profile with recent transactions
export suspicious transactions
no database used