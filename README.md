## GraphQL & REST-Based Data Integration Pipeline – Tokopedia & TurnBackHoax.id (2023)

Developed an automated **dual-source web scraping and data integration pipeline** combining **GraphQL API extraction** (Tokopedia) and **pseudo REST API HTML parsing** (TurnBackHoax.id).  
The unified dataset supports **text mining, misinformation detection (NLP)**, and **e-commerce trend analysis**.

<table>
<tr>
<td align="center"><img src="https://raw.githubusercontent.com/rizalarb/Dual-Source-WebScraping-FactCheck-Builder/main/assets/tokopedia-dashboard.png" width="260"/><br><sub><b>Tokopedia Product Data</b><br>Automated product collection via GraphQL API</sub></td>
<td align="center"><img src="https://raw.githubusercontent.com/rizalarb/Dual-Source-WebScraping-FactCheck-Builder/main/assets/turnbackhoax-scraper.png" width="260"/><br><sub><b>TurnBackHoax Dataset</b><br>Structured text extraction via pseudo REST scraping</sub></td>
<td align="center"><img src="https://raw.githubusercontent.com/rizalarb/Dual-Source-WebScraping-FactCheck-Builder/main/assets/eda-insights.png" width="260"/><br><sub><b>Exploratory Data Insights</b><br>Trends, topics, and correlation overview</sub></td>
</tr>
</table>

---

### 🔍 Highlights

- **GraphQL API Integration (Tokopedia)**  
  Built a dynamic scraper that sends GraphQL payloads to Tokopedia’s `https://gql.tokopedia.com/graphql/SearchProductQueryV4`.  
  Extracted detailed product attributes such as **name, price, rating, shop, and city** through a single GraphQL endpoint.

- **Pseudo REST API Scraping (TurnBackHoax.id)**  
  Implemented an **HTML parser using BeautifulSoup** to simulate REST-style HTTP GET requests,  
  extracting structured data fields — **title, date, category, and fact-check results** — from TurnBackHoax.id articles.

- **Data Integration**  
  Unified both sources into a structured **Pandas DataFrame**, enabling direct use for **NLP preprocessing**, **EDA**, or **BI dashboards**.

- **Automated Export & Visualization**  
  Implemented an automated `.xlsx` export pipeline for live storage and used **Matplotlib** to visualize price clustering and misinformation trends.

- **Scalability**  
  Provided modular scraping functions extendable to other **Indonesian e-commerce** or **fact-checking websites**.

---

### 🧠 Tools & Technologies
`Python`, `Requests`, `BeautifulSoup`, `Pandas`, `JSON`, `LXML`, `GraphQL`, `Excel`, `Matplotlib`

---

### 🧾 Example Outputs

#### Tokopedia (GraphQL API)
| Product | Price | Rating | Shop | City |
|----------|--------|---------|------|------|
| Samsung Galaxy A15 | 2,350,000 | 4.8 | Samsung Official | Jakarta |
| Infinix Note 30 | 2,099,000 | 4.7 | GadgetZone | Bandung |

#### TurnBackHoax.id (Pseudo REST API Scraping)
| Title | Category | Date | Summary |
|--------|-----------|------|----------|
| [SALAH] Foto “ORANG CHINA berseragam BRIMOB” | Hoax | July 2020 | Clarified and debunked by fact-check team |
| [BENAR] Info resmi vaksinasi COVID-19 | Fact | May 2021 | Verified through government data |

---

### ⚙️ Methodological Workflow

1️⃣ **GraphQL API Request (Tokopedia)**  
→ Define search parameters  
→ Send GraphQL payload (`query`, `variables`)  
→ Extract JSON response fields  

2️⃣ **Pseudo REST HTML Parsing (TurnBackHoax.id)**  
→ Crawl article pages with `requests.get()`  
→ Parse HTML using `BeautifulSoup`  
→ Extract title, date, category, and text  

3️⃣ **Data Cleaning & Integration**  
→ Normalize nested JSON and HTML tables  
→ Merge into unified dataset  

4️⃣ **Export & Visualization**  
→ Save to `.xlsx`  
→ Analyze price distributions and misinformation categories using Pandas + Matplotlib  

---

### 🚀 Potential Applications

- **Misinformation Detection** — Train NLP models (e.g., BERT) for hoax/non-hoax classification.  
- **Market Intelligence** — Correlate product pricing with topic trends.  
- **Public Awareness Research** — Analyze misinformation influence on consumer behavior.

---

[Back to Top](#ahmad-rizal-bayhaqi--data-analyst--visualization-specialist)
