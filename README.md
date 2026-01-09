# 📊 AI Market Liquidity Intelligence System

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-complete-success.svg)
![Data Source](https://img.shields.io/badge/data-yahoo%20finance-orange.svg)

## 📋 Project Overview

**AI Market Liquidity Analyser Intelligence System** is an open-source, Python-based financial market analysis tool designed for educational and research purposes. The system provides comprehensive liquidity analysis across multiple asset classes using historical market data from Yahoo Finance (yfinance).

The tool analyses **60+ assets** including equity indices, sector ETFs, single stocks, fixed income instruments, forex pairs, commodities, derivatives, and cryptocurrencies from **2000 to present**. Users can input any trading date for analysis, making it valuable for historical market research and liquidity pattern recognition.

## 📊 Project Status

This is a **completed portfolio project** that I'm sharing publicly to demonstrate my skills.

## 🌐 Live Dashboard

**Note:** This project includes a web dashboard interface that GitHub cannot display properly.

👉 **Experience the full interactive version:** [hamza-choudhury.github.io](https://hamza-choudhury.github.io)

The live site showcases all interactive features, charts, and controls that make this project unique.

## 🎯 Key Features

### 1. **Multi-Asset Coverage**
- **60+ Assets** across 8 major asset classes
- **Global coverage**: US, Europe, Asia, and emerging markets
- **Diverse instruments**: Stocks, bonds, currencies, commodities, crypto
- **Sector analysis**: All 11 major S&P 500 sectors via ETFs

### 2. **Comprehensive Liquidity Metrics**
- **Spread %**: Bid-ask spread proxy calculated as (High-Low)/Close
- **Volume Ratio**: Today's volume vs 30-day average
- **Market Depth**: Simulated order book depth (deterministic random)
- **Asset Classification**: Automated mapping to 8 asset classes

### 3. **Advanced Analytics Suite**
- **Yield Curve Analysis**: Treasury yield analysis with recession signals
- **Correlation Matrix**: 30+ asset correlation heatmap with strong pair identification
- **Time-Series Trend Analysis**: 20-day momentum and volatility across key assets
- **Sector Rotation Heatmap**: Sector ETF liquidity ranking
- **Machine Learning Predictions**: Spread direction forecasting using Random Forest
- **Stress Testing**: Portfolio impact simulation for +50bps rate shock
- **AI Market Intelligence**: Integrated AI analysis combining all modules

### 4. **Professional Interactive Dashboard**
- **13+ interactive charts** with professional styling
- **Dynamic HTML dashboard** with chart selector navigation
- Asset class performance comparisons
- Top/bottom liquidity rankings with visual bars
- Correlation insights with strong pair detection
- Trend analysis with performance metrics
- Risk assessment visualisation
- Executive summary with action recommendations

### 5. **Enhanced AI Intelligence System**
- **8 comprehensive market scenarios** with dynamic selection
- **Module integration**: Combines liquidity + correlation + trends + ML
- **Customised recommendations**: Real asset names and metrics
- **Risk alerts**: Multi-dimensional risk assessment
- **Trading desk intelligence**: Institutional-style execution strategy

## 📅 Date Flexibility

The system accepts **any trading date from 2000 to present** with intelligent validation:
- Validates trading days (no weekends/bank holidays)
- Falls back to previous trading days if needed
- Handles timezone differences and market closures
- User gets 3 attempts to input valid dates

## 📈 Analysis Modules

### **1. Liquidity Metrics Analysis**
**Why it's important**: Liquidity determines execution costs and market efficiency. Tight spreads indicate healthy markets, while wide spreads suggest potential stress or inefficiency.

### **2. Yield Curve Analysis**
**Why it's important**: Yield curve shape (normal/inverted) is a leading economic indicator. Inverted curves often precede recessions, while steep curves suggest expansion.

### **3. Correlation Matrix Analysis**
**Why it's important**: Identifies relationships between assets for portfolio construction, risk management, and hedging strategies. Strong correlations reduce diversification benefits.

### **4. Time-Series Trend Analysis**
**Why it's important**: Identifies market momentum, trend participation, and volatility patterns across key assets. Helps distinguish trending vs range-bound markets.

### **5. Sector Rotation Analysis**
**Why it's important**: Identifies which sectors have best/worst liquidity, helping understand market rotation and risk appetite.

### **6. Machine Learning Predictions**
**Why it's important**: Attempts to forecast tomorrow's spread direction based on historical patterns, providing forward-looking insights with accuracy reporting.

### **7. Stress Testing**
**Why it's important**: Simulates market shocks to understand portfolio vulnerabilities and risk exposures across different asset classes.

### **8. Comprehensive AI Market Intelligence**
**Why it's important**: Integrates all module outputs into unified trading recommendations with execution strategy, risk management, and immediate action plans.

## 🤖 Machine Learning Implementation

### **ML Model Details:**
- **Algorithm**: Random Forest Classifier (30 estimators, max_depth=5)
- **Features**: 
  - Spread_Proxy, Volume_MA5, Volume_MA20, Volatility, Volatility_20
  - Returns, Momentum_5, Momentum_10 (8 total features)
- **Target**: Binary classification (spread increase/decrease next day)
- **Train/Test Split**: 80/20 chronological split
- **Evaluation**: Accuracy score on test set with feature importance
- **Data Requirements**: Minimum 20 days of history, prefers 60+ days

### **ML Limitations:**
1. **Limited Historical Data**: Uses 90 days of history per asset
2. **Simple Features**: Technical indicators only, no fundamental data
3. **Independent Models**: Each asset modelled separately
4. **No Cross-Validation**: Simple chronological split only
5. **Binary Classification**: Doesn't predict magnitude of spread changes
6. **Feature Fallback**: Uses heuristics when ML fails

## 🧠 Enhanced AI Analysis System

### **How It Works:**
The enhanced AI system integrates **all analysis modules** with dynamic scenario selection:

1. **Multi-dimensional Assessment**: Evaluates liquidity, correlation, trends, volume, and volatility
2. **Dynamic Scenario Selection**: 8 comprehensive market scenarios with rules-based logic
3. **Integrated Insights**: Combines data from all 17 modules
4. **Customised Recommendations**: Real asset names, specific spread values, and timing advice
5. **Risk Integration**: Incorporates ML predictions and stress test results
6. **Professional Reporting**: Generates comprehensive institutional reports

### **Market Scenarios:**
1. **EXCELLENT_LIQUIDITY_HIGH_CORRELATION**: Synchronised markets with optimal liquidity
2. **EXCELLENT_LIQUIDITY_LOW_CORRELATION**: Diverse markets with tight spreads
3. **GOOD_LIQUIDITY_TRENDING_MARKET**: Clear directional trends with good execution
4. **GOOD_LIQUIDITY_RANGE_BOUND**: Sector rotation in range-bound conditions
5. **NORMAL_MARKET_HIGH_VOL**: Elevated volatility with normal liquidity
6. **NORMAL_MARKET_LOW_VOL**: Low volatility grind environment
7. **POOR_LIQUIDITY_DIVERGENT**: Illiquid markets with divergent behaviour
8. **HIGH_VOLUME_LOW_CORRELATION**: Active but diverse market drivers

### **AI Analysis Outputs:**
- **Liquidity Score**: 0-100 based on spread metrics
- **Market Diagnosis**: Integrated assessment across all dimensions
- **Execution Strategy**: Order types, timing, and sizing recommendations
- **Risk Management**: Stop losses, hedging, and position sizing
- **Immediate Actions**: Specific assets to trade/avoid with rationales
- **Next Steps**: Follow-up timing and catalyst monitoring

## 🛠️ System Architecture (17 Modules)

### **Module Breakdown:**

| Module | Function | Description |
|--------|----------|-------------|
| **1** | Setup | Installs dependencies and imports libraries |
| **2** | Asset Universe | Defines 60+ tickers across 8 asset classes |
| **3** | Date Input | Interactive date validation with fallback |
| **4** | Asset Class Mapper | Maps tickers to asset classes |
| **5** | Data Fetcher | Fetches price/volume data from yfinance with fallbacks |
| **6** | Metric Calculator | Calculates liquidity metrics |
| **7** | Main Processing Loop | Processes all tickers with progress tracking |
| **8** | Results Compilation | Creates DataFrame and saves to CSV |
| **9** | Yield Curve Analysis | Treasury yield analysis and curve interpretation |
| **10** | Sector Rotation | Sector ETF liquidity heatmap |
| **11** | ML Predictions | Machine learning for spread forecasting |
| **12** | Stress Testing | +50bps yield shock portfolio impact |
| **13** | Correlation Matrix | Asset return correlation analysis |
| **14** | Time-Series Trends | Historical trend and volatility analysis |
| **15** | AI Market Intelligence | Comprehensive AI analysis integration |
| **16** | Executive Summary | One-page actionable summary |
| **17** | Professional Dashboard | Interactive HTML dashboard with 13+ charts |

## 📊 Interactive Dashboard Features

### **Dashboard Components:**
1. **Asset Class Coverage**: Distribution across asset classes
2. **Spread by Asset Class**: Visual comparison of liquidity
3. **Liquidity Leaders/Laggards**: Top 5 best/worst assets
4. **Correlation Insights**: Average correlation and strong pairs
5. **Trend Analysis**: Market momentum and participation
6. **ML Predictions**: Accuracy and prediction distribution
7. **Volume Anomalies**: High/low volume asset counts
8. **Stress Test Impact**: Portfolio vulnerability visualisation
9. **Yield Curve**: Treasury curve shape analysis
10. **Sector ETF Liquidity**: Sector spread comparison
11. **Spread Distribution**: Histogram of spread values
12. **Activity vs Cost Scatter**: Volume vs spread relationship
13. **Asset Class Performance**: Comparative returns
14. **Risk Assessment**: Integrated risk metrics

### **Dashboard Navigation:**
- **Interactive Chart Selector**: Dropdown menu for easy navigation
- **User Instructions**: Guided analysis workflow
- **Professional Styling**: Institutional-grade visual design
- **Responsive Layout**: Adapts to different screen sizes
- **Real-time Metrics**: Live calculation displays

## 📈 Output Files Generated

The system creates **multiple output files** per analysis:

### **Data Files:**
1. `liquidity_results_YYYY-MM-DD.csv` - Raw metrics for all assets
2. `ml_predictions_YYYY-MM-DD.csv` - Machine learning predictions
3. `ml_feature_importance_YYYY-MM-DD.csv` - ML feature weights
4. `ml_summary_YYYY-MM-DD.json` - ML performance summary
5. `stress_test_YYYY-MM-DD.json` - Stress test results
6. `correlation_matrix_YYYY-MM-DD.csv` - Correlation matrix
7. `strong_correlations_YYYY-MM-DD.csv` - Strong correlation pairs
8. `correlation_stats_YYYY-MM-DD.json` - Correlation statistics
9. `trend_analysis_YYYY-MM-DD.csv` - Trend performance data
10. `trend_stats_YYYY-MM-DD.json` - Trend statistics

### **Visualisation Files:**
1. `sector_heatmap_YYYY-MM-DD.png` - Sector liquidity visualisation
2. `correlation_matrix_YYYY-MM-DD.png` - Correlation heatmap
3. `time_series_analysis_YYYY-MM-DD.png` - Trend charts

### **Report Files:**
1. `ai_comprehensive_analysis_YYYY_MM_DD.txt` - Detailed AI analysis report
2. `executive_summary_YYYY-MM-DD.txt` - One-page executive summary
3. `market_liquidity_dashboard_YYYY-MM-DD.html` - Interactive HTML dashboard

## ⚠️ Limitations & Important Notes

### **Data Limitations:**
1. **Free Data Source**: Uses Yahoo Finance free tier with potential:
   - Delayed data (15-20 minutes for equities)
   - Inconsistent availability for some tickers
   - Potential data gaps or errors
   - Limited historical depth for some assets

2. **Simulated Metrics**:
   - Market Depth uses deterministic random numbers
   - Volume averages based on 30-day history only
   - Spread calculation is a proxy (not actual bid-ask)

3. **Historical Data Only**:
   - Cannot analyse real-time or intraday data
   - Limited to daily frequency
   - No after-hours or pre-market data

4. **Date Data Gaps**: Even when a date is validated as a trading day, Yahoo Finance may not have data for all assets due to:
   - Historical data gaps in their database
   - Delisting or symbol changes over time
   - Regional market holidays not accounted for
   - API rate limiting or temporary unavailability
   The system will skip assets with missing data and continue processing others.

### **Technical Limitations:**
1. **Single-threaded Processing**: Processes assets sequentially (~2-3 minutes runtime)
2. **Memory Intensive**: Loads data for all 60+ assets simultaneously
3. **API Rate Limits**: May hit yfinance rate limits during peak times
4. **No Data Caching**: Fetches fresh data each run

### **Analysis Limitations:**
1. **Spread Proxy**: High-Low range ≠ actual bid-ask spread
2. **ML Model Simplicity**: Basic Random Forest with limited features
3. **Correlation Timeframe**: Uses only 1-month returns for correlations
4. **Stress Test Simplicity**: Static sensitivities, single scenario
5. **No Fundamental Analysis**: Price/volume only, no earnings or news

## 🚀 Usage Guide

## 📋 Prerequisites

- Python 3.8+
- Internet connection (for data fetching)
- 2GB RAM minimum
- Jupyter Notebook environment

## 🚀 Installation & Running

The notebook will auto-install required packages:
- yfinance
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

Simply run all cells in the notebook sequentially. No manual installation needed - everything is included.

## 📖 Usage

1. Run all cells in the notebook
2. Enter a date when prompted (YYYY-MM-DD format)
3. Wait ~2 minutes for processing
4. View results in terminal and output files
5. Check generated charts and reports

### Important Notes

- ✅ **Functional & Complete**: The code works as shown
- ⚠️ **No Planned Updates**: This is a finished project
- 🚫 **No Support**: I won't be answering questions or providing help
- 📚 **Educational Purpose**: For learning and demonstration only

### For Potential Employers

This project demonstrates my ability to:
- Build comprehensive financial analysis tools
- Work with multiple data sources and APIs
- Implement machine learning in practical applications
- Create professional visualisations and reports
- Structure complex projects with clear modular design
- Document technical projects thoroughly
- Apply financial concepts in code implementation

Feel free to examine the code as an example of my work.

## 📄 MIT License Explained

**What the MIT License means for users:**

- ✅ **Free forever**: No cost to use
- ✅ **No restrictions**: Can be used for commercial or personal projects
- ✅ **Can modify**: Users can adapt the code to their needs
- ✅ **Can distribute**: Users can share their modified versions
- ❌ **No warranty**: Provided "as is" without guarantees
- 📝 **Simple requirement**: Just keep the original copyright notice

This is a permissive license used by major companies like Microsoft, Facebook, and Google for their open-source projects.

## 💰 Optional Support (Post & Forget)

**Important**: This is a **"post and forget"** open-source project. The developer provides this tool for free and does not plan regular updates or feature additions.

### Optional Appreciation

If you find this tool valuable and want to show appreciation:

- **PayPal**: https://paypal.me/HChoudhury0 (One-time or recurring donations)
- **Buy Me A Coffee**: https://buymeacoffee.com/hchoudhury (Small appreciation payments)

### How Funds Could Potentially Be Used

If sufficient appreciation is shown, it **could potentially** inspire:

1. **Live Data APIs**: Integration of real-time data sources
2. **Enhanced ML Models**: More sophisticated algorithms
3. **Cloud Deployment**: Web interface version
4. **Additional Features**: More asset classes, new analyses

**However**: No promises, guarantees, or expectations. This is purely optional appreciation for a free, open-source educational tool.

## ⚖️ Critical Legal Disclaimer

### FOR EDUCATIONAL AND RESEARCH PURPOSES ONLY

**THIS SOFTWARE IS NOT FINANCIAL ADVICE. USE AT YOUR OWN RISK.**

1. **Educational Tool Only**: This software is designed for learning about financial markets, data analysis, and programming. It is not intended for real trading or investment decisions.

2. **Not Financial Advice**: All analyses, recommendations, and outputs are hypothetical and for educational demonstration. They do not constitute financial advice, investment recommendations, or trading signals.

3. **Accuracy Not Guaranteed**: The data comes from free public sources and may contain errors, delays, or inaccuracies. The analysis methods are simplified educational examples and may not reflect real market conditions or professional practices.

4. **Past Performance**: Historical analysis does not guarantee future results. Market conditions change, and past patterns may not repeat.

5. **Your Responsibility**: You are solely responsible for any decisions you make. Always consult with qualified financial professionals before making any investment decisions.

6. **No Warranty**: This software is provided "as is", without warranty of any kind, express or implied. The author is not responsible for any losses, damages, or financial consequences resulting from the use of this software.

7. **No Liability**: The author accepts no liability for any direct, indirect, incidental, special, exemplary, or consequential damages arising from the use of this software.

8. **Academic Focus**: This tool is designed for students, researchers, and hobbyists to learn about market analysis techniques, Python programming, and data science applications in finance.

**By using this software, you acknowledge that you have read, understood, and agree to these terms. If you do not agree, do not use this software.**

---

## 🏛️ About This Project

This project was created as a demonstration of technical skills in:
- Financial market analysis
- Python programming and data science
- Machine learning implementation
- Data visualisation
- Professional documentation

It showcases practical application of theoretical concepts in a complete, working system suitable for inclusion in a technical portfolio.

---

**Made for the open-source and financial education community**

*Empowering learning through accessible market analysis tools*

---

Licensed under the MIT License. See LICENSE file for details.
