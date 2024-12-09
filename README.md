# Formulation of the Korean Fear Index Reflecting Foreign Investment : Validation Using Market Timing Strategies

## 0. Special Thanks
This study was inspired by research conducted based on _'EMP 전략'_ by Hanhwa Investment and Securities.

## I. Research Background and Objective

### 1.1 Background
**1.1.1 Limitaitons of VKOSPI**
The VKOSPI, introduced by KRX in 2009, serves currently as Korea's fear index measuring the implied volatility of KOSPI200 options.
Limitations of VKOSPI:
  - Does not fully reflect the market fear and shows unstable correlations with the market.
  - Low liquidity in KOSPI200 options and weak correlation with global indices like VIX (US) and VSTOXX (Europe).

**1.1.2 Foreign Investment in the Korean Financial Market**
High foreign investor proportion in KOSPI (33%) and KOSDAQ (10%) markets
The recent underperformance of KOSPI, centered around Samsung Electronics' stock price, has highlighted the selling trends of foreign investors and the medium-to-long-term risks associated with Samsung Electronics.
  
  <img width="427" alt="image" src="https://github.com/user-attachments/assets/2485dc16-c861-450d-b88c-76fb9ee3d605">
  

When assessing fear in the Korean market alone, there is a possibility that the index may lag behind the impact of foreign investors.
This underscores the need for an index that reflects :
  1. Korean market characteristics.
  2. Foreign investors' influence on the Korean market.

### 1.2 Objective
- Development of a Korea-specific Fear Index Reflecting the Characteristics of the Korean Market
- Development of a Foreign Fear Index Considering the Trends of Foreign Investors in the Korean Market
- If foreign investors' fear precedes fear in the Korean market, validate the effectiveness of a market timing strategy leveraging this time gap.

## II. Korean Fear Index

### 2.1 CNN Fear & Greed Index
The CNN Business Fear & Greed Index quantifies investor sentiment, measuring the level of fear and greed present in the stock market. It ranges from 0 to 100, where 0 represents extreme fear and 100 represents extreme greed. The index is calculated as an equally weighted arithmetic average of daily values from seven technical indicators, each ranging between 0 and 100.

<img width="404" alt="image" src="https://github.com/user-attachments/assets/c3efd7fe-258c-4cdf-a735-b8d3ce8e575d">

<img width="437" alt="image" src="https://github.com/user-attachments/assets/c4e4ee30-4cb6-446b-a721-f63cfa248a2b">

The seven technical indicators of the CNN Fear & Greed Index were reconstructed to suit the Korean market, forming the foundation for developing a Korea-specific Fear Index.

### 2.2 Variable Declaration
- Adaptation of CNN's 7 indicators for the Korean market:
  1. Market Momentum: KOSPI price relative to its 125-day moving average.
  2. Stock Strength: Ratio of 52-week high vs. low stocks in KOSPI.
  3. Stock Breadth: McClellan Summation Index (MSI) for KOSPI.
  4. Put/Call Option Ratio: Ratio of KOSPI200 options.
  5. Market Volatility: VKOSPI.
  6. Safe Haven Demand: Spread between 10-year treasury yields and KOSPI returns.
  7. Junk Bond Demand: Spread between high-yield and low-risk corporate bonds.

  ![image](https://github.com/user-attachments/assets/0e36b797-40f7-482b-aefd-3fbddc29888b)


### 2.3 Data
- Historical data from August 6, 2013, to November 8, 2024.
- Preprocessing methods:
  - Robust Scaling: Minimize outlier impact.
  - MinMax Scaling: Normalize variables between 0 and 1.
  - Adjusted arithmetic averaging to combine variables.


  <img width="418" alt="image" src="https://github.com/user-attachments/assets/70ae0894-23d6-4b77-863e-5e207cabab3e">


## III. Foreign Fear Index

### 3.1 Variable Description
- Based on foreign net purchases of KOSPI stocks adjusted by USD/KRW exchange rate.
- Reflects foreign investors' confidence and fund flows.

### 3.2 Granger Causality
- Test if foreign fear index influences Korean fear index significantly.

### 3.3 Variable Description
- Refined with macroeconomic variables:
  1. 3-Year Interest Rate Spread: US-Korea bond yield differences.
  2. Dollar Index (DXY): Global economic conditions and currency fluctuations.

### 3.4 Index Strengthening Variable
**3.4.1 3-Year Interest Rate Spread:**
- Captures cost differences for investors between US and Korea.

**3.4.2 Dollar Index:**
- Measures relative strength of USD against other major currencies.

### 3.5 Granger Causality Comparison and Stationary Testing
- Granger causality tested before and after index strengthening.
- Stationarity validated with Augmented Dickey-Fuller (ADF) and KPSS tests.

## IV. Backtesting

### 4.1 Literature Review and Comparison
- Previous models used single fear indices (e.g., VIX).
- This study incorporates both Korean and foreign indices for better market representation.

### 4.2 Backtesting Procedure and Results
- Methodology:
  - Data Period: 2013-08-06 to 2024-11-08.
  - Initial capital: 100M KRW split into stocks (60%) and cash (40%).
  - Strategy:
    - Buy when both indices signal extreme fear.
    - Sell during extreme greed.
  - Performance Metrics: Lower volatility, higher returns compared to KOSPI-only benchmarks.

## V. Conclusion

### 5.1 Insights
- Foreign fear index leads the Korean index, validating its predictive power.
- Market timing strategy based on fear indices demonstrates:
  1. Reduced risk.
  2. Enhanced returns.

### 5.2 Limitations
- Excludes trading costs, slippage, and tax impacts.
- Heavily reliant on US-centric factors (e.g., dollar index, US-Korea bond spread).
- Neglects diverse foreign investor profiles (e.g., Europe, China).

