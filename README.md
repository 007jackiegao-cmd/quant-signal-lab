# Quant Signal Lab

Momentum backtesting with turnover costs, equity curves, drawdown and rolling volatility. The browser and Python implementations use the same calculation.

[Open app](https://007jackiegao-cmd.github.io/quant-signal-lab/)

## Run

```sh
npm ci
npm run dev
```

```sh
python3 backtest.py --seed 17 --lookback 21 --cost-bps 5
python3 -m unittest -v test_backtest.py
node test-parity.js
npm run build
```

The sample contains 505 generated prices (seed 17). Exposure for period `t` uses prices through `t-1`; costs are charged on absolute position changes. Change the lookback and cost in the app to compare results.

`backtest.py` contains the Python calculation. `research-ui.js` contains the JavaScript calculation and charts. Tests cover signal timing, costs, drawdown and parity across four configurations.
