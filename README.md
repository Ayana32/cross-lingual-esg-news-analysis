# cross-lingual-esg-news-analysis
## 1. Extreme Cross-National ESG Coverage Divergence

### UK: Climate Monoculture
- **Environmental**: 92.6% ████████████████████████████  
- **Social**: 5.2% ██  
- **Governance**: 2.2% █  

**Key observations**
- Nearly all ESG coverage focuses on the climate crisis  
- Social and Governance issues are largely marginalized  
- Reflects political prioritization and media agenda-setting  

---

### Korea: Holistic ESG Approach
- **Environmental**: 45.3% ██████████████  
- **Governance**: 36.1% ███████████  
- **Social**: 18.5% █████  

**Key observations**
- Balanced distribution across all three ESG pillars  
- Governance driven by chaebol reform and corporate transparency needs  
- Social dimension rooted in long-standing CSR culture  

---

## 2. 2024 Emerging Trends

### 🇰🇷 Korea: ESG Institutionalization Wave
- **Certification Boom (+44%)**  
  → Rapid increase in ESG certification acquisition  
- **Rating System Maturation (+15%)**  
  → Intensified competition for MSCI AAA ratings  
- **Financial Integration (+11%)**  
  → ESG metrics increasingly tied to quarterly earnings  

**Overall shift**  
- From *“nice to have”* → *“must report”*

---

### 🇬🇧 UK: Politicization & Daily Life Connection
- **Political Earthquake (+116%)**  
  → Trump election dominates ESG discourse  
  → 54 mentions in November alone  
- **Food System Focus (+24%)**  
  → Meat production and dietary impact enter mainstream climate debate  
- **EV Reality Check (+22%)**  
  → Shift from optimism to practical concerns  
  → “Too expensive”, “too heavy”, infrastructure gaps  

---

## 3. Strategic Cultural Interpretations

| Aspect | Korea ESG | UK ESG |
|------|----------|--------|
| Concept | Corporate Comprehensive Responsibility | Climate Crisis Response Driver |
| Focus | Institutional Standards (K-ESG, GRI) | Regulatory Compliance & Political Activism |
| Trend | Standardization & Certification | Politicization & Personalization |

---

## 4. Methodology

### Model
- **Neural Topic Modeling**
- **BERTopic** + **Multilingual BERT embeddings**

### Data Collection
- **Period**: January 1, 2023 – December 31, 2024  
- **Sources**:  
  - UK: *The Guardian* API (quarterly balanced sampling)  
  - Korea: Major national news outlets  
- **Volume**: ~40,000 articles per country  

### Preprocessing Pipeline
- **Deduplication**  
  - TF-IDF + Cosine Similarity (threshold = 0.8)  
  - Removed 393 duplicate UK articles (1.1%)  

- **Length Filtering**  
  - UK: 400–10,000 characters  
  - Korea: 200–10,000 characters  

- **Content Type Filtering**  
  - Article-only  
  - Excluded liveblogs and interactive content  

### ESG Classification
- Keyword-based scoring + manual validation  
- **UK Environmental**: strict filtering  
  - Initial 92.6% refined to remove non-environmental content  
- **Social & Governance**: rule-based + keyword validation  

Content Type: Article-only (excluded liveblogs, interactives)
ESG Classification: Keyword-based scoring + manual validation

UK Environmental: Strict filtering (92.6% → refined to remove non-environmental)
Social & Governance: Rule-based + keyword validation
