## GA-Optimized-SMA-Strategy

### Overview
This project implements a **genetic algorithm (GA)-optimized simple moving average (SMA) crossover trading strategy**. Inspired by the approach outlined in the paper "An Efficient Implementation of the Backtesting of Trading Strategies" by Jiarui Ni and Chengqi Zhang, this project utilizes GA to systematically identify optimal parameters for maximizing the **Sharpe Ratio** of a trading strategy on Google stock data (GOOG). The project features efficient backtesting, strategy analysis, and performance reporting.

### Project Structure

- **`genetic_algorithm.py`**: Contains the genetic algorithm framework for optimizing SMA parameters.
- **`backtesting.py`**: Includes functions to backtest the trading strategy and calculate key performance metrics like Sharpe Ratio, Annualized Return, and Maximum Drawdown.
- **`data/`**: Stores data used for backtesting (Yahoo Finance historical stock prices).
- **`plots/`**: Contains generated plots showing the strategy's performance and the evolution of SMA parameters.
- **`results/`**: Stores backtesting results for each generation of the GA and the final optimized strategy metrics.

### Key Features

- **SMA Crossover Strategy**: Generates buy/sell signals based on crossovers of short and long SMAs.
- **Genetic Algorithm Optimization**: Utilizes GA to evolve SMA window parameters over multiple generations, selecting for the highest Sharpe Ratio.
- **Comprehensive Backtesting**: Backtests each parameter set to assess performance, with metrics such as total return, annualized return, and max drawdown.
- **Results Visualization**: Visualizes the optimized strategy’s equity curve, parameter evolution, and other performance indicators.

### Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/GA-Optimized-SMA-Strategy.git
cd GA-Optimized-SMA-Strategy
```

Install the necessary dependencies (see `requirements.txt`):

```bash
pip install -r requirements.txt
```

### Usage

1. **Data Collection**: Ensure the required data is available in the `data/` folder. You can use `pandas_datareader` to download stock data if needed.

2. **Running the Genetic Algorithm Optimization**:
   Run the GA optimization script to find optimal SMA windows:
   ```bash
   python genetic_algorithm.py
   ```

3. **Backtesting**:
   After identifying the optimal parameters, run the backtesting module:
   ```bash
   python backtesting.py
   ```

4. **Visualize Results**:
   Visualizations of the equity curve, performance metrics, and optimization process are saved in the `plots/` folder.

### Example Results

The GA-optimized strategy achieved the following key performance metrics:

- **Return**: 39.0%
- **Annualized Return**: 38.8%
- **Sharpe Ratio**: 1.12
- **Maximum Drawdown**: -18.1%

For detailed performance analysis, refer to the results and plots in the `results/` and `plots/` folders.

### References

- **Jiarui Ni and Chengqi Zhang**: ["An Efficient Implementation of the Backtesting of Trading Strategies"](https://www.researchgate.net/publication/220945302_An_Efficient_Implementation_of_the_Backtesting_of_Trading_Strategies), which inspired the approach to backtesting and optimization.

### License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
