# EV Giants Showdown: Tesla vs. BYD Investment Analysis (2020-2024)

## 1. Problem Definition
### Target Audience
Designed for **Individual Investors** evaluating the Electric Vehicle (EV) sector.

### The Business Challenge
As the EV price war intensifies, investors must choose between two different leaders:
- **Tesla (TSLA):** High-tech brand premium and software-driven margins.
- **BYD (1211.HK):** Manufacturing scale, vertical integration, and diverse product lines.

**Core Question:** Which company demonstrates better financial resilience and R&D efficiency?

---

## 2. Methodology & Data Sources
### Data Sourcing
- **Primary Source:** Real-time financial data via `yfinance` (Yahoo Finance API).
- **Local Dataset:** To comply with reproducibility requirements, a synchronized dataset `ev_data_backup.csv` is included in this repository.

### Hybrid Data Logic (Technical Execution)
Due to frequent API rate limits observed during development, this product includes a **Robust Fallback Mechanism**. The script prioritizes live API fetching but automatically switches to the local CSV dataset if the connection is restricted, ensuring **100% uptime** for reviewers and users.

### Tech Stack
- **Python:** Data processing and analysis.
- **Pandas:** Financial statement cleaning and CSV management.
- **Seaborn/Matplotlib:** Professional investment visualization.

---

## 3. Visual Dashboard
![Tesla vs BYD Analysis](analysis_chart.png)

---

## 4. Key Insights & Interpretation
Based on the visualized data:
- **Profitability:** Tesla's gross margin peak in 2022 has narrowed due to strategic price cuts. In contrast, BYD shows strong resilience, likely due to its vertically integrated battery supply chain.
- **Innovation (R&D):** BYD’s R&D intensity has shown a significant upward trend, recently surpassing Tesla's in terms of revenue percentage, indicating aggressive investment in next-gen battery tech.
- **Market Growth:** Both giants face a slowdown from 2021 peaks, but BYD maintains higher relative growth in the global mass-market segment.

---

## 5. How to Run
1. Ensure `ev_data_backup.csv` is in the same directory as the notebook.
2. Open `Analysis.ipynb` in JupyterLab or Google Colab.
3. Run all cells. The script will automatically detect the best available data source and render the dashboard.

---

## 6. Reflection & Professional Practice
### AI Disclosure
This project was developed with the assistance of AI (Gemini) for the following professional purposes:
- Troubleshooting `yfinance` API rate-limiting and designing the error-handling logic.
- Optimizing data visualization aesthetics using `Seaborn` themes.
- Structuring the GitHub repository and documentation to meet academic "Excellent" standards.

### Limitations & Future Work
- **Data Granularity:** The current analysis uses annual figures. Future iterations will incorporate quarterly data to capture short-term market volatility.
- **Scope Expansion:** Integrating social sentiment analysis (e.g., from X or Reddit) would provide a more holistic view of brand health beyond pure financials.
- **Technical Improvement:** Transitioning from CSV to a local SQLite database would enhance data handling for larger, multi-company comparisons.
