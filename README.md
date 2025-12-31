# 📊 Clustering Brazilian Stocks with DBSCAN (B3)

This project applies **unsupervised learning (DBSCAN)** to cluster the **most traded stocks in the Brazilian Stock Exchange (B3)**, aiming to identify **investment profiles, risks, and opportunities** based on financial indicators.

The analysis focuses on **data extraction, filtering, clustering, and visualization**, combining financial reasoning with machine learning techniques.

---

## 🗂️ Data Source

- **Website:** Fundamentus  
- **URL used:** https://www.fundamentus.com.br/resultado.php  

The webpage provides a comprehensive table with **financial and market indicators** for all stocks traded on B3.

For this project:
- Only the **50 most traded stocks** (based on average daily volume over the last 2 months) are selected.
- A **CSV file** is automatically generated to facilitate further analysis and reproducibility.

---

## ⚙️ Methodology

### 1. Data Extraction and Preprocessing
- Automated scraping of Fundamentus data.
- Selection of key valuation and liquidity indicators.
- Export of a cleaned dataset to CSV format.

### 2. Benchmark Filtering (Noise Reduction)

To speed up the analysis and remove low-quality stocks, a benchmark filter is applied:

1. **Minimum P/E ratio:** 0.1  
2. **Maximum P/E ratio:** 20  
3. **Minimum Dividend Yield (DY):** 4%  
4. **Minimum Liquidity Index:** 1  

This step helps exclude illiquid or financially distorted stocks before clustering.

---

## 🤖 Clustering with DBSCAN

- **Algorithm:** DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
- **Goal:** Group stocks with similar financial characteristics without predefining the number of clusters.
- DBSCAN is particularly useful for:
  - Identifying natural groupings
  - Handling outliers (“junk stocks”)
  - Capturing non-linear relationships between indicators

---

## 📈 3D Visualization

The selected indicators are visualized in **3D space**, allowing a clearer interpretation of stock groupings based on:
- Valuation
- Liquidity
- Dividend returns
- Growth potential

This visualization helps distinguish clusters associated with **risk profiles and investment strategies**.

---

## 🔎 Identifying Opportunities and Insights

From the clustering and 3D visualization, two main groups stand out:

### 1. Safe Bets / Cash Cows
- Fair P/E ratio  
- High liquidity  
- High dividend yield  

**Examples:**  
- DIRR3  
- CYRE3  
- ITSA4  

These stocks tend to offer **stable returns and lower risk**.

---

### 2. Growth Candidates
- Fair P/E ratio  
- Low dividend yield  
- High liquidity  

Lower DY may indicate reinvestment in expansion and scale.

**Examples:**  
- ENGIE3  
- TAEE11  
- LREN3  

These stocks may offer **higher growth potential** in the medium to long term.

---

## ⚠️ Limitations and Future Work

- The analysis is **not exhaustive** and does not replace fundamental or sector-specific research.
- Future extensions could include:
  - Sector-level clustering (e.g., construction, retail, energy)
  - Time-series analysis of indicators
  - Integration with macroeconomic or market sentiment data

---

## 📌 Conclusion

This project demonstrates how **unsupervised learning and financial indicators** can be combined to support **investment screening and exploratory analysis** in emerging markets, offering a scalable framework for future refinements.
