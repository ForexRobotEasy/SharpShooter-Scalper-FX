# SharpShooter Scalper FX Expert Advisor

This Expert Advisor has been developed by the Forex Robot Easy Team. For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/sharpshooter-scalper-fx-review-achieve-exceptional-forex-results/). Please note that ForexRobotEasy is not the official developer of this product. We are only showcasing sample code that can work as described in this product. To find the official developer of this product, please use MQL5.

## Global Variables
- `ticket`: Order ticket number
- `stopLoss`: Stop Loss level
- `takeProfit`: Take Profit level

## Functions
- `openBuyOrder(double price)`: Function to open a buy order
- `openSellOrder(double price)`: Function to open a sell order
- `calculateLevels()`: Function to calculate stop loss and take profit based on the dynamic ratio

## Start Function
The `OnTick()` function is the starting point of the Expert Advisor. It checks if there are no open orders. If there are no open orders and the current symbol is USD/CAD, it calls the `calculateLevels()` function to calculate the stop loss and take profit levels. It then opens a buy order at the current bid price and a sell order at the current ask price.

## How It Works
The Expert Advisor relies on the `OnTick()` function, which is called every time there is a new tick in the market. It checks if there are any open orders using the `OrdersTotal()` function. If there are no open orders, it proceeds to check if the current symbol is USD/CAD using the `Symbol()` function.

If the current symbol is USD/CAD, it calls the `calculateLevels()` function to calculate the stop loss and take profit levels based on the dynamic ratio. The dynamic ratio is calculated by dividing the account balance by the account equity.

The `calculateLevels()` function sets the stop loss level as the dynamic ratio multiplied by 10, and the take profit level as the dynamic ratio multiplied by 20. The `NormalizeDouble()` function is used to round the levels to the appropriate number of decimal places.

After calculating the stop loss and take profit levels, the Expert Advisor opens a buy order at the current bid price using the `openBuyOrder()` function, and a sell order at the current ask price using the `openSellOrder()` function. The order volume is set to 0.1, and the order comments are set as 'Buy Order' and 'Sell Order' respectively.

Please note that this code is a sample and may need to be modified or customized to fit specific trading strategies or requirements. It is recommended to consult the official developer of the product or use MQL5 for further customization or development.

For more information about the SharpShooter Scalper FX Expert Advisor, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/sharpshooter-scalper-fx-review-achieve-exceptional-forex-results/).
