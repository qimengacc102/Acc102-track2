# Acc102-track2
# Apple Inc. Long‑Term Financial Health Dashboard

[![GitHub Repo](https://img.shields.io/badge/GitHub-ACC102_Track2-blue?logo=github)](https://github.com/qimengacc102/Acc102-track2)
[![WRDS](https://img.shields.io/badge/Data-WRDS_Compustat-green)](https://wrds-www.wharton.upenn.edu/)

**XJTLU | IBSS | ACC102 AI‑Driven Data Analytics | Track 2**

![Dashboard Preview](figures/apple_dashboard.png)

---

## 1. Problem & User

**Analytical Problem**  
How has Apple Inc.’s capital structure shifted from a debt‑free growth company to a leveraged cash‑return machine? This project moves beyond headline P/E ratios to examine the drivers of Apple’s **100%+ ROE** and evolving risk profile.

**Target Users**  
- **Finance Students**: A reproducible template for WRDS‑based ratio analysis.  
- **Retail Investors**: A visual explanation of Apple’s changing balance sheet.

---

## 2. Data

| Item | Description |
| :--- | :--- |
| **Source** | WRDS – Compustat North America (Annual Fundamentals) |
| **Library & Table** | `comp.funda` |
| **Company** | Apple Inc. (GVKEY `001690`) |
| **Period** | 1980 – 2025 (46 fiscal years) |
| **Access Date** | 2026‑04‑23 |
| **Key Variables** | Revenue, net income, total assets, total liabilities, total equity, current assets, current liabilities, shares outstanding, closing price |

---

## 3. Methods (Python Workflow)

1. **Extract** – Connected to WRDS via `wrds.Connection()` and ran parameterized SQL to fetch 22 fundamental fields.  
2. **Clean** – Dropped rows with missing `sale`, `ni`, `at`; filtered zero/negative denominators.  
3. **Compute** – Calculated 9 ratios across Profitability, Liquidity, Leverage, and Valuation.  
4. **Visualize** – Generated 2×2 dashboard using `matplotlib` and `seaborn`.

**Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `wrds`

---

## 4. Key Findings (Data‑Backed)

- 🚀 **ROE > 100% Since 2015** – ROE surged primarily due to **share buybacks reducing equity**, not just net income growth.  
- 📉 **Current Ratio Fell from 5.0 → 1.2** – Apple shifted from hoarding cash to efficient working capital management.  
- 🏦 **Debt‑to‑Equity Rose from 0 → 1.5** – Apple issued first long‑term debt in 2013 to fund shareholder returns.  
- 📊 **Gross Margin Stability** – Gross margins consistently exceeded **35%**, reflecting strong pricing power.

---

## 5. How to Run

### Prerequisites
- Python 3.8+
- Active WRDS Account (or use provided `apple_financial_metrics.csv` fallback)
- Jupyter Notebook

### Steps
```bash
git clone https://github.com/qimengacc102/Acc102-track2.git
cd Acc102-track2
pip install -r requirements.txt
jupyter notebook "ACC102_track2.ipynb"
6. Product Link / Demo
 
- GitHub Repo: https://github.com/qimengacc102/Acc102-track2

- Demo Video: [Your Mediasite/Bilibili Link]
 
 
 
7. Limitations & Future Work
 
Limitations
 
- Annual data only; quarterly fluctuations not captured.

- No peer comparison (e.g., Microsoft, Alphabet).
 
Future Work
 
- Add competitor benchmarking.

- Extend to quarterly data (comp.fundq).

- Deploy as interactive Streamlit dashboard.
## 8. AI Disclosure

| Field | Detail |
| :--- | :--- |
| **Tool** | DeepSeek|
| **Date** | 2026-04-23 |
| **Specific AI Contributions** | 1. **README Structure**: Helped organize the README sections according to the ACC102 Track 2 rubric.<br>2. **WRDS Query Optimization**: Suggested parameterized SQL to avoid hard‑coding identifiers.<br>3. **Pandas Code Refinement**: Helped debug column‑renaming order and corrected plotting field names.<br>4. **Visualization Enhancements**: Recommended adding reference lines to improve readability.<br>5. **Insight Phrasing**: Helped refine bullet points to be concise and data‑backed. |
| **Independent Work Statement** | All financial logic, ratio formulas, data cleaning criteria, SQL query design, and final interpretation of results were independently developed, verified, and fully understood by me. No AI‑generated content was used without my complete review and comprehension. |
