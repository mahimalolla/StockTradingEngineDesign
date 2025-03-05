# Stock Trading Engine

## Overview
This project implements a **real-time stock trading engine** that simulates buying and selling stock orders. Orders are matched based on their price and ticker symbol, and matched trades are visualized using a **line graph**.

## Features
- Supports up to **1024 different stock tickers**.
- Matches **Buy and Sell orders** dynamically in real-time.
- Uses **multithreading** for efficient order matching.
- Utilizes a **queue-based system** for handling orders.
- **Visualizes** matched trade prices over time using **Matplotlib**.

## How It Works
1. **Buy and Sell Orders** are randomly generated.
2. Orders are stored in separate **queues** (FIFO structure).
3. A background thread continuously matches orders:
   - A Buy order is matched with the lowest Sell order of the same stock ticker **if the Buy price is greater than or equal to the Sell price**.
   - The trade quantity is determined by the smaller of the two order quantities.
4. Matched trades are stored and **plotted as a line graph** to visualize stock price trends.

## Installation & Requirements
Ensure you have **Python 3.x** installed along with the required libraries.

### Install Dependencies
```sh
pip install matplotlib
```

## Running the Simulation
To start the stock trading engine, execute:
```sh
python stock_trading_engine_design_mahimanjali_lolla.py
```

## Expected Output
- **Console Output:**
  ```
  Matched: Stock25, Quantity: 50, Price: 450.25
  Matched: Stock982, Quantity: 30, Price: 320.75
  Matched: Stock10, Quantity: 100, Price: 275.00
  ...
  ```
- **Graph Output:**
  - A **line graph** showing trade price trends over time.
  
## Modifications
- Adjust `MAX_ORDERS` in `stock_trading_engine.py` to control the number of orders.
- Modify `simulate_stock_transactions()` to generate different stock behaviors.


