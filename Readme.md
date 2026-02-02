# EquityLens

**EquityLens** is a lightweight, static stock data visualization tool designed to explore how price trends and rank-based interpretations behave across different data sources — especially when data is incomplete or inconsistent.

The project emphasizes **data reliability, interpretability, and visualization choices**, rather than prediction or trading signals.

**Live demo (GitHub Pages):**  
<ADD YOUR GITHUB PAGES LINK HERE>

---

## Why this project exists

In many analytical domains, conclusions are shaped not only by available data, but by how **missing, unreliable, or selectively available data is handled**.

EquityLens was built as a compact exploratory tool to:
- compare long-term stock price trends across multiple public APIs
- visualize rank movement over time relative to benchmark thresholds (Top 50 / 100 / 200)
- avoid implicit interpolation when data is missing
- fail transparently and fall back to simulated data when access constraints occur

The focus is on **analytical honesty**, not optimization or forecasting.

---

## Data availability and limitations

Data coverage varies significantly across market data providers, particularly under free-tier access.

- Some symbols may not return historical data depending on the selected provider and access limits.
- Full symbol coverage and extended historical depth typically require paid API plans offered by respective providers.
- When data retrieval fails due to missing keys, invalid symbols, or API constraints, the application switches to simulated data to preserve the visualization workflow.

---

## Rank visualization design

The secondary chart intentionally allows **temporal discontinuities**, displaying rank data only when a symbol meets the selected benchmark threshold.

This approach:
- avoids misleading interpolation across absent data points
- highlights meaningful index entry and exit events
- focuses attention on periods relevant to benchmarking and comparative analysis

Rather than forcing continuity, the design prioritizes **decision-relevant visibility**.

---

## Key characteristics

- Fully static, one-page web application  
- No backend, authentication, or server-side storage  
- User-supplied API keys (stored locally in browser)  
- Graceful fallback to simulated data  
- Print- and PDF-friendly layout  

---

## Technology stack

- HTML5 / CSS  
- JavaScript  
- Chart.js  
- Tailwind CSS (CDN)  

No build step is required.

---

## Future directions

Possible future extensions include:
- POST-based data ingestion for external datasets
- streamed PDF generation from output data
- integration into analytical pipelines
- packaging as a Node.js module for programmatic use

These are exploratory directions rather than committed roadmap items.

---

## Intended use

This project is shared as an **analytical artifact**, not a production trading system.

It may be of interest to:
- data scientists and analysts
- researchers working with time-series or rank-based data
- developers concerned with visualization integrity and edge cases

---

## Author

**Saurabh Gayali, PhD**  
Computational Biologist & Scientific Data Specialist  

- Website: https://www.thevisualstoriesstudio.com  
- GitHub: https://github.com/saurabhgayali  

---

## License

MIT License
