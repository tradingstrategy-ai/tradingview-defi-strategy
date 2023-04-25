# TradingView to TradingStrategy.ai algorithmic DeFi trading strategy conversion

This is an example Github repository how to convert a TradingView based PineScript algorithmic 
trading strategy to TradingStrategy.ai Python format.

- Execute your strategy in a counterparty risk free manner 
- Broker free, direct to exchange
- Have 100% control of your strategy market data and live execution
- [Low trading fees on efficient decentralised markets](https://tradingstrategy.ai/blog/most-efficient-market-is-on-a-public-blockchain-and-decentralised)
- Convert your trading algorithm to a on-chain fund
- Benefits of rich Python quant finance libraries like `pandas_ta` and `quantmetrics`

This example repository was made for Avalanche Summit II workshop.

## About the example strategy

The example strategy is presented as a 

- [PineScript source file](./bollinger_band_example_tradingview_strategy.pine) 
- [Backtesting Jupyter Notebook for Trading Strategy](./bollinger_band_example_defi_strategy.ipynb)

The example strategy is a Bollinger Band based strategy. 
It is recommended to be used with

- Volatile cryptocurrencies - tested with MATIC/USD
- Long only - suitable for [DEX spot markets](https://tradingstrategy.ai/glossary/spot-market)
- Daily OHCLV candles

### Notable differences between Python and PineScript

- Python data is presented as Pandas DataFrame's - the de facto core unit of any data science,
  whereas TradingView uses its own data format.
- Python time series are zero indexed. Zero is the oldest item and minus one is the latest.

PineScript:

```pinescript

```

Python:

```python

```

### Example of TradingView

- Import the script to TradingView
- Choose XXX/USD market
- Shwo the backtest results

### Example of Jupyter notebook

- Run in Visual Studio Code, as described below


## About trading on decentralised finance

### DEX trading fees

You have four elements of fees

- Blockchain transaction costs or [gas fees]()
  - Going towards zero and neglible in the future
- Trading fee, which consists of
  - [Liquidity provider fee](https://tradingstrategy.ai/glossary/liquidity-provider) 
  - ...and [protocol fee](https://tradingstrategy.ai/glossary/protocol-fee) 
  - Usually 0.05% for large Uniswap v3 pools, otherwise 0.25% - 0.30% on [AMMs](https://tradingstrategy.ai/glossary/amm)
  - [Compares to 0.60% taker fee on Coinbase, others]()
- [Price impact](https://tradingstrategy.ai/glossary/price-impact)
  - Unlike on order book exchanges, this is very easy to historically backtest on AMMs due to deterministic nature of the price
    based on liquidity
- [Slippage](https://tradingstrategy.ai/glossary/slippage)
  - Price change between signing your transction and having a block producer to include it in a block 
  - Also important for [MEV protection](https://tradingstrategy.ai/glossary/mev)
  - Usually orders are signed with maximum slippage
- AMM and [CLMM](https://tradingstrategy.ai/glossary/clmm) based DEXes do not have slippage

## Preqrequisites

### Skills

- Basic experience in cryptocurrencies
- Basic experience in trading
- Experience in TradingView's PineScript
- Junior software developer level experience in Python

### Software 

- Python 3.10
- [Poetry package manager for Python](https://tradingstrategy.ai/community)
- Git

## Installation

Make a git clone of this repository and then run `poetry` to create a Python environment for your project.

```shell
poetry shell
poetry install
```

### API key

When you run the notebook for the first time, you will be prompted to register to give an API key for Trading Strategy datasets.

## Running backtest notebooks from terminal

Running the backtesting notebook in a terminal is the most robust, though not that useful method 

- Works always - you see if your code works
- Opens any charts separate windows in a web browser
- But it's very hard to work with notebooks in a terminal
- Using shell for notebooks allows e.g. you to use `ipdb` breakpoints in Python code.

How to run:

```shell
ipython example.ipynlb
```

This will open couple of browser tabs and print out the results

```
Trading period length                       0 days
Return %                                     0.00%
Annualised return %                              -
Cash at start                           $10,000.00
Value at end                            $10,000.00
Trade volume                                 $0.00
Position win percent                             -
Total positions                                  0
Won positions                                    0
Lost positions                                   0
Stop losses triggered                            0
Stop loss % of all                               -
Stop loss % of lost                              -
Take profits triggered                           0
Take profit % of all                             -
Take profit % of won                             -
Zero profit positions                            0
Positions open at the end                        0
Realised profit and loss                     $0.00
Portfolio unrealised value                   $0.00
Extra returns on lending pool interest       $0.00
Cash left at the end                    $10,000.00
Average winning position profit %                -
Average losing position loss %                   -
Biggest winning position %                       -
Biggest losing position %                        -
Average duration of winning positions       0 days
Average duration of losing positions        0 days
LP fees paid                                 $0.00
LP fees paid % of volume                     0.00%
Average position:                            0.00%
Median position:                             0.00%
Most consecutive wins                            0
Most consecutive losses                          0
Biggest realized risk                        0.00%
Avg realised risk                            0.00%
Max pullback of total capital                0.00%
Max loss risk at opening of position         0.00%
```

## Running backtest notebooks with Visual Studio Code

First start a server from command line

```shell
poetry shell
jupyter server 
```

Copy the kernel URL with the secret token from the console output.] 

Open any notebook in Visual Studio Code.

Use `Select Kernel` at the top right of the screen, choose Remot Jupyter Kernel, add URL option.
Paste in the URL  (should b e automatically pasted).

Run the notebook.

## Next steps

- [Join Trading Strategy community Discord for discussion and questions](https://tradingstrategy.ai/docs/)
- [View our learning material for algorithmic trading](https://tradingstrategy.ai/docs/learn/index.html)
- [Study other strategy backtesting examples and code samples](https://tradingstrategy.ai/docs/programming/index.html)