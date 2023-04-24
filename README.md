# TradingView to TradingStrategy.ai algorithmic trading strategy conversion

This is an example Github repository how to convert a TradingView based PineScript algorithmic 
trading strategy to TradingStrategy.ai Python format.

- Execute your strategy in a counterparty risk free manner 
- Get lower fees on decentralised exchanges
- Convert your trading algorithm to a on-chain fund

This example repository was made for Avalanche Summit II workshop.

## Preqrequisites

### Skills

- Basic experience in cryptocurrencies
- Basic experience in trading
- Experience in TradingView's PineScript
- Junior software developer level experience in Python

### Software 

- Python 3.10
- Poetry package manager
- Git

## Installation

Make a git clone of this repository and then run `poetry` to create a Python environment for your project.

```shell
poetry shell
poetry install
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

## Running backtest notebooks from terminal

This allows e.g. you to use `ipdb` breakpoints in Python code. 

```shell
ipython example.ipynlb
```

This will print out the results

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
