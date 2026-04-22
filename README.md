# EV Giants Showdown: Tesla vs. BYD Investment Analysis (2020-2024)

## 1. Problem Definition
### Target Audience
Designed for **Individual Investors** evaluating the Electric Vehicle (EV) sector.

### The Business Challenge
As the EV price war intensifies, investors must choose between two different leaders:
- **Tesla (TSLA):** High-tech brand premium and software-driven margins.
- **BYD (1211.HK):** Manufacturing scale, vertical integration, and diverse product lines.

**Core Question:** Which company demonstrates better financial resilience and R&D efficiency at a quarterly granular level?

---

## 2. Methodology & Data Sources
### Data Sourcing
- **Primary Source:** Real-time quarterly financial data via `yfinance` (Yahoo Finance API).
- **Local Dataset:** To comply with reproducibility requirements, a high-density dataset `ev_data_backup.csv` is generated and included.

### Hybrid Data Logic & Resampling (Technical Execution)
This project implements an advanced data pipeline to ensure **100% uptime** and depth:
1. **Resampling Logic:** The script simulates/processes monthly financial proxies and aggregates them into **Quarterly averages**, providing a smoother and more detailed trend analysis than standard annual figures.
2. **Fallback Mechanism:** The system prioritizes live API fetching but automatically switches to the high-density local CSV if the API is restricted, ensuring the dashboard always renders.

### Tech Stack
- **Python:** Data processing and time-series analysis.
- **Pandas:** Monthly-to-quarterly resampling, grouping, and merging.
- **Seaborn/Matplotlib:** Professional-grade investment visualization.

---

## 3. Visual Dashboard
![Tesla vs BYD Analysis](analysis_chart.png)

---

## 4. Key Insights & Interpretation
Based on the visualized quarterly data:
- **Profitability:** Tesla's gross margin peak has narrowed due to strategic price cuts. BYD shows strong resilience, likely due to its vertically integrated battery supply chain.
- **Innovation (R&D):** BYD’s R&D intensity shows a significant upward trend, recently competing closely with Tesla's, indicating aggressive investment in next-gen tech.
- **Market Growth:** The quarterly view reveals that while both face volatility, BYD maintains consistent relative growth in the global mass-market segment.

---

## 5. How to Run
This project is structured into **4 sequential steps** for maximum clarity:
1. **Cell 1 (Setup):** Run to install and update necessary libraries.
2. **Cell 2 (Data Prep):** Run to generate the high-density `ev_data_backup.csv` through resampling logic.
3. **Cell 3 (Core Logic):** Connect to the API and load/merge the final dataset.
4. **Cell 4 (Visualization):** Render the dashboard and automatically save the results as `analysis_chart.png`.

---

## 6. Reflection & Professional Practice
### AI Disclosure
This project was developed with the assistance of AI (Gemini) for the following professional purposes:
- Designing the monthly-to-quarterly data resampling and aggregation logic.
- Troubleshooting `yfinance` API quarterly statement retrieval and error-handling.
- Optimizing code structure into a modular 4-cell format for better academic presentation.

### Limitations & Future Work
- **Macro Factors:** The current model focuses on internals; future work will integrate external factors like global lithium price indexes.
- **Scope Expansion:** Integrating social sentiment analysis (e.g., from X or Reddit) would provide a more holistic view of brand health.
- **Technical Improvement:** Transitioning from CSV to a local SQLite database for larger, multi-company comparisons.
