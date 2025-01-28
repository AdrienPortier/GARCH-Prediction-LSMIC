# GARCH-Prediction-LSMIC

## Introduction
This project was carried out as part of the **LSM Investment Club** (LSMIC), in collaboration with **Jonathan Kojovi** and under the supervision of a project manager. It is part of the **quant team** activities, whose main goal is the management of a portfolio exceeding €25,000.

The objective of this project was to present prediction tools to club members. Although the models explored, such as **GARCH**, are more suitable for short-term forecasts than the long-term strategies favored by the club, we also examined metrics like **Value at Risk (VaR)** and **Expected Shortfall (ES)** to quantify risks.

This project was conducted alongside our academic commitments during October and November 2024. The results were subsequently presented to all members of the club.

## Objectives
- Implement the GARCH model on historical data of a selected stock (TotalEnergies).
- Compare and analyze risk metrics: VaR and ES.
- Evaluate the performance of the models over different time horizons.

While this project has an educational scope, it highlights modern techniques used in the industry for risk management and financial time series analysis.

## Technologies Used
- **Main Language**: Python
- **Key Libraries**:
  - `pandas`: Data manipulation.
  - `numpy`: Numerical computations.
  - `arch`: Implementation of GARCH models.
  - `yfinance`: Historical stock data retrieval.
  - `matplotlib` and `seaborn`: Data and results visualization.
  - `scipy`: Statistical tools.

## Key Results
### Value at Risk (VaR) and Expected Shortfall (ES)
We calculated VaR and ES at 1% and 5% risk levels based on the log-returns of the **TotalEnergies** stock. These metrics demonstrated that Expected Shortfall provides a better assessment of extreme risks.

### GARCH Model
The Generalized Autoregressive Conditional Heteroskedasticity (GARCH) model was used to model conditional volatility.
- Several residual distributions were compared, including the normal distribution and the Student’s t-distribution.
- Model performance was evaluated using directional accuracy, likelihood, and mean squared error (MSE).

### E-GARCH Variant
An asymmetric extension of the model, **E-GARCH**, was implemented to capture leverage effects. However, the results showed similar performance to the standard GARCH model, with no significant improvement in modeling extremes.

## Critiques and Limitations
- GARCH models perform well for short-term predictions but lose relevance as the time horizon increases.
- The underlying assumptions, such as stationarity and residual distribution, are not always valid under real market conditions.

## Project Structure
- **Main Notebook**: Contains the implementation and results.
- **Data**: Historical price data for TotalEnergies over four years (imported using `yfinance`).
- **Visualizations**: Graphs for VaR, ES, volatility predictions, autocorrelations, and QQ-Plots.

## Contributors
- **Jonathan Kojovi** ([LinkedIn](https://www.linkedin.com/in/jonathan-kojovi-b3a4a221a/?originalSubdomain=be))
- **Adrien Portier** ([LinkedIn](https://www.linkedin.com/in/adrien-portier/))

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/AdrienPortier/GARCH-Prediction-LSMIC.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Launch the Jupyter notebook to explore the analyses.
