# Portfolio Optimization using Monte Carlo Simulation

## 📌 Project Overview
This project is a financial data analysis and optimization tool that employs **Monte Carlo Simulations** to determine the optimal asset allocation for a stock portfolio. By acquiring historical data using the **yfinance** API, the project analyzes stock performance from **2018 to the present** to find the best balance between risk (volatility) and return.

The core objective is to maximize the **Sharpe Ratio**, providing a data-driven recommendation for how to distribute capital across a diversified portfolio of 10 major U.S. stocks.

## 🚀 Key Features

### 1. Data Acquisition & Preprocessing
* **Automated Data Fetching:** Utilizes the **`yfinance`** library to download real-time historical stock data.
* **Stocks Analyzed:** A diverse mix of Tech, Finance, Healthcare, and Industrial stocks:
    * Amazon (AMZN)
    * JPMorgan Chase (JPM)
    * Meta Platforms (META)
    * Procter & Gamble (PG)
    * Alphabet/Google (GOOGL)
    * Caterpillar (CAT)
    * Pfizer (PFE)
    * Exelon (EXC)
    * John Deere (DE)
    * Johnson & Johnson (JNJ)
* **Data Cleaning:** Handles missing values and normalizes stock prices for accurate comparison.

### 2. Exploratory Data Analysis (EDA)
* **Interactive Visualizations:** Uses **Plotly Express** to create dynamic line charts for:
    * Adjusted Closing Prices.
    * Daily Returns.
    * Growth of individual portfolio positions over time.
* **Statistical Analysis:** Computes daily percentage returns and visualizes price trends over the selected period.

### 3. Monte Carlo Simulation
* **Simulation Engine:** The notebook runs **10,000 simulation runs**, randomly assigning different weights to the assets in the portfolio.
* **Metric Calculation:** For every run, the following metrics are calculated:
    * **Expected Annual Return**
    * **Annual Volatility (Risk)**
    * **Sharpe Ratio**
* **Optimization:** The algorithm identifies the specific set of weights that yields the maximum Sharpe Ratio.

### 4. Results Visualization
* **Efficient Frontier:** Generates a scatter plot of Volatility vs. Return for all 10,000 simulations.
* **Optimal Portfolio Highlight:** Visually highlights the "Optimal Point" (Maximum Sharpe Ratio) in red on the Efficient Frontier graph.

## 🛠️ Technologies Used
* **Python 3.x**
* **yfinance:** For fetching historical market data.
* **Pandas & NumPy:** For data manipulation, dataframe handling, and numerical calculations.
* **Plotly Express:** For creating interactive financial charts.
* **Matplotlib & Seaborn:** For static data visualization (e.g., correlation heatmaps).

## 💻 Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/Portfolio-Optimization-using-Monte-Carlo-Simulation.git](https://github.com/yourusername/Portfolio-Optimization-using-Monte-Carlo-Simulation.git)
    ```

2.  **Install required dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn plotly yfinance requests
    ```

3.  **Run the Notebook:**
    Open the Jupyter Notebook to execute the simulation.
    ```bash
    jupyter notebook "Portfolio_Optimization_using_Monte_Carlo.ipynb"
    ```

## 📊 Example Results
After running the simulation, the notebook outputs the optimal portfolio metrics, similar to:
* **Best Portfolio Metrics Based on 10,000 Runs:**
    * **Portfolio Expected Annual Return:** ~20.33%
    * **Portfolio Volatility:** ~20.45%
    * **Sharpe Ratio:** ~0.85
    * **Return on Investment:** ~272.97%


