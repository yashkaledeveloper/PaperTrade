## Paper Trading Platform

A full-stack paper trading application that simulates stock trading using virtual money.
Users can place buy/sell orders, manage holdings, track positions, and view P&L using live or mock stock prices.


## Features

### Authentication

* User signup and login
* JWT-based protected routes

### Wallet

* Default virtual balance per user
* Automatic balance updates on trades

### Orders

* Market buy and sell order simulation
* Balance and quantity validation
* Executed order tracking

### Portfolio

* Holdings with average buy price calculation
* Realized and unrealized P&L
* Automatic updates after each trade

### Visualization

* Portfolio distribution charts
* Performance insights

### Stock Prices

* Live prices via free APIs
* Mock price fallback for simulation

---

## Tech Stack

### Frontend

* React
* Material UI
* JavaScript
* Axios

### Backend

* Node.js
* Express.js
* MongoDB

---

## Core Trade Logic

### Buy Order

* Validate user and wallet balance
* Fetch current stock price
* Deduct balance
* Create or update holding with average price
* Mark order as executed

### Sell Order

* Validate holding quantity
* Credit wallet balance
* Update or remove holding
* Calculate realized P&L

---

### Database Models

* User
* Wallet
* Order
* Holding

Models are separated to maintain clarity and scalability.

---

### Disclaimer

This is a paper trading simulation.
No real money. No real trading.