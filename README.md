# Gold Veritas MT5 ReadMe File

Gold Veritas MT5 is an automated Forex advisor that is designed to trade on the MetaTrader 5 platform. This code is a sample implementation of the trading logic used in the Gold Veritas MT5 expert advisor. Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product.

## Product Description

Gold Veritas MT5 is an expert advisor that specializes in trading gold (XAU) against various currency pairs. It opens pending orders for four currency pairs: XAUUSD, XAUJPY, XAUAUD, and XAUEUR. The expert advisor uses a buy stop order to enter trades.

The expert advisor opens a buy stop order for each currency pair at a price that is 10 pips above the current bid price. The stop loss (SL) and take profit (TP) levels are set at 100 pips above and below the entry price, respectively.

The expert advisor also includes a feature to close all open trades within a specified lifespan. The lifespan is set to 5 hours (18000 seconds) by default. If a trade has been open for longer than the lifespan, it will be closed automatically.

## How It Works

1. The expert advisor initializes by calling the OnInit() function. No additional initialization code is included in this sample code.
2. The OnTick() function is called on every tick of the market. It calls the OpenPendingOrders() function to open pending orders for all currency pairs.
3. The OpenPendingOrders() function calls the OpenPendingOrder() function for each currency pair to open a buy stop order.
4. The OpenPendingOrder() function calculates the entry price, stop loss, and take profit levels for the specified currency pair. It then calls the OrderSend() function to open the buy stop order.
5. If the buy stop order is successfully opened, the expert advisor prints a success message. Otherwise, it prints an error message.
6. The CloseTransactions() function is called in the OnTrade() event handler. It iterates through all open orders and checks if their symbols match the specified currency pairs. If a trade has been open for longer than the specified lifespan, it is closed using the OrderClose() function.
7. If a trade is successfully closed, the expert advisor prints a success message. Otherwise, it prints an error message.

## Product Review and Trading Results

For detailed reviews and trading results of the official Gold Veritas MT5 expert advisor, please visit the following link: [Gold Veritas MT5 Review - Automated Forex Advisor for Quiet Hours](https://forexroboteasy.com/forex-robot-review/gold-veritas-mt5-review-automated-forex-advisor-for-quiet-hours/)

Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please use the MQL5 platform.
