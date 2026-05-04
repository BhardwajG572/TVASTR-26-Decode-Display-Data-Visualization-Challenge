# 🌍 Global Ripple Effects: The Russia-Ukraine War Economic Shock

> **Submission for TVASTR ’26: Decode & Display – Data Visualization Challenge**

**Author:** Gaurav Bhardwaj  
**Domain:** Quantitative Economics & Data Science  

## 📌 Executive Summary
This project analyzes how the Russia–Ukraine war reshaped global commodity markets, inflation patterns, and financial outcomes across countries and sectors. Through an interactive Power BI dashboard, this analysis visualizes the cause-and-effect transmission mechanisms of the shock, proving that the economic fallout was not uniform.

Instead, the shock propagated unevenly through global markets depending on structural factors such as energy dependence, currency strength, and geopolitical positioning.

---

## 📊 Key Analytical Insights

### 1. Global Commodity Shock (The Transmission Channel)
The war disrupted global supply chains, particularly in energy and agricultural markets. The dashboard reveals that **EU gas prices experienced the largest spike, followed by oil, while wheat prices increased more gradually.** This indicates that the primary transmission channel of the shock was energy markets, which then fed into broader inflation across the global economy. The persistence of elevated prices suggests a prolonged inflationary environment, rather than a temporary price disturbance.

### 2. Uneven Inflation Across Countries (The Vulnerability Filter)
While commodity prices increased globally, inflation outcomes differed significantly across countries. This uneven impact is driven by three structural factors:
*   **Import Dependence:** Countries heavily reliant on imported energy and food faced higher costs when global prices surged.
*   **Currency Weakness:** Because commodities are priced in US Dollars, depreciation of local currencies amplified inflation by increasing domestic import costs.
*   **Economic Resilience:** Developed economies absorbed shocks via policy interventions, while emerging economies experienced the most severe inflation spikes, confirming that global shocks are filtered through domestic vulnerabilities.

### 3. Winners vs. Losers (Financial Redistribution)
The war led to a redistribution of economic value rather than a uniform global decline:
*   **The Winners:** Defense companies (e.g., Rheinmetall) saw massive growth due to increased military spending. Additionally, nations like India benefited from trade arbitrage—importing discounted Russian crude oil, refining it, and exporting it at market prices.
*   **The Losers:** Russia’s domestic stock market (MOEX) experienced a sharp decline reflecting sanctions and capital outflows. Similarly, highly import-dependent emerging economies faced severe economic contraction.

---

## 🖥️ Dashboard Architecture & Navigation
The Power BI file (`.pbix`) is structured into interactive storyboard pages:

*   **Page 1: The Synchronized Shock (Macro Overview)**
    *   Features a multi-line indexed time-series chart normalizing Oil, Gas, and Wheat to a base of 100 in January 2022.
    *   Tracks the immediate percentage surges in commodities vs. the collapse of the MOEX index and the boom of Defense stocks.
*   **Page 2 and 3: The Ripple Map (Geospatial Impact) & Winners and Lossers **
    *   An interactive global heatmap mapping peak inflation rates.
    *   Includes a dynamic "Country Impact Profile" side-panel and a Top 10 "Losers" leaderboard to highlight the hardest-hit nations.

---

## ⚙️ Technical Methodology & Data Engineering
To ensure robust "Industry-Grade" quantitative analysis, the following methodologies were applied:

*   **Data Modeling:** Utilized a strict **Star Schema** architecture with a centralized `DimDate` table driving 1-to-many relationships across disparate commodity, index, and inflation fact tables.
*   **DAX Optimization:** Built advanced DAX measures to normalize time-series data using dynamic `CALCULATE` and `ALL()` filter context overrides, preventing blank values during market holidays.
*   **Financial Accuracy:** Utilized **Adjusted Close** prices for all equity indices to account for dividends and corporate actions, ensuring an accurate reflection of total economic value generation.
