# Polygon Trading Bot

This is a Python-based trading bot that retrieves and stores NASDAQ-100 tickers, monitors market status, and prepares for trading operations during premarket and regular trading hours using the Polygon API.

## Features

- Fetches NASDAQ-100 tickers during early market hours using Financial Modeling Prep API.
- Stores tickers in a MongoDB database.
- Monitors market status (open, closed, early hours) using Polygon API.
- Logs events and errors for easy debugging.
- Can be extended to execute custom trading strategies.

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yeonholee50/polygon-trading-bot.git
    cd polygon-trading-bot
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Set up MongoDB:
   - You will need a MongoDB cluster. If you don’t have one, sign up at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) and set up your cluster.
   - Ensure you have the MongoDB connection string, and create a database for storing the stock data.

## Configuration

1. Rename `config_template.py` to `config.py` and provide your API keys and MongoDB credentials:

    ```python
    POLYGON_API_KEY = "your_polygon_api_key"
    FINANCIAL_PREP_API_KEY = "your_fmp_api_key"
    MONGO_DB_USER = "your_mongo_user"
    MONGO_DB_PASS = "your_mongo_password"
    ```

## Usage

To run the bot, simply execute:

```bash
python client.py
