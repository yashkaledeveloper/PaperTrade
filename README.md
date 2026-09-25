# Paper Trading Platform

A full-stack **paper trading application** that simulates stock trading using virtual money. Users can securely manage their wallet, place buy/sell orders, track holdings, and monitor realized/unrealized P&L using live or mock stock prices.

## Key Features

* **Authentication:** User signup/login with JWT-based protected routes.
* **Virtual Wallet:** Default virtual balance with automatic updates after trades.
* **Trading:** Market buy/sell simulation with balance and quantity validation.
* **Portfolio Management:** Holdings, average buy price, realized P&L, and unrealized P&L.
* **Visualization:** Portfolio distribution and performance insights.
* **Stock Prices:** Live market prices through free APIs with mock-price fallback.
* **Order Tracking:** Maintains executed trade history for each user.

## Tech Stack

**Frontend:** React, Material UI, JavaScript, Axios
**Backend:** Node.js, Express.js
**Database:** MongoDB
**Authentication:** JWT

## Core Trade Flow

**Buy:** Validate user → Fetch stock price → Validate balance → Deduct balance → Create/update holding → Record executed order.

**Sell:** Validate holding → Fetch stock price → Credit wallet → Update/remove holding → Calculate realized P&L → Record executed order.

## Database Models

* `User` — authentication and user information
* `Wallet` — virtual balance
* `Order` — executed buy/sell transactions
* `Holding` — current portfolio positions

Models are separated to keep the application modular and scalable.

## Installation & Running

### 1. Clone the repository

```bash
git clone https://github.com/yashkaledeveloper/PaperTrade.git
cd paper-trading-platform
```

### 2. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

Start the backend:

```bash
npm run dev
```

### 3. Frontend Setup

Open a new terminal:

```bash
cd frontend
npm install
npm run dev
```

The application will be available at the URL shown by Vite, usually:

```text
http://localhost:5173
```

Backend API runs on:

```text
http://localhost:5000
```

## Project Highlights

This project demonstrates **full-stack development, REST API design, JWT authentication, MongoDB data modeling, transaction logic, portfolio calculations, API integration, and responsive React UI development**.

> **Disclaimer:** This is a paper trading simulation using virtual money. It does not execute real trades or involve real money.
