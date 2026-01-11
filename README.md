# cross-lingual-esg-news-analysis
## Key Findings
### 1. Extreme Cross-National ESG Coverage Divergence
UK: Climate Monoculture
Environmental: 92.6% ████████████████████████████
Social:         5.2% ██
Governance:     2.2% █

Nearly all ESG coverage focuses on climate crisis
Social and Governance issues largely marginalized
Reflects political prioritization and media focus

Korea: Holistic ESG Approach
Environmental: 45.3% ██████████████
Governance:    36.1% ███████████
Social:        18.5% █████

Balanced distribution across all three pillars
Governance driven by chaebol reform needs
Social rooted in corporate CSR culture

### 2. 2024 Emerging Trends
Korea: ESG Institutionalization Wave

Certification Boom (+44%): Companies rushing to obtain ESG certifications
Rating System Maturation (+15%): MSCI AAA race intensifies
Financial Integration (+11%): ESG metrics tied to quarterly earnings reports
Shift: From "nice to have" → "must report"

UK: Politicization & Daily Life Connection

Political Earthquake (+116%): Trump election dominates discourse (54 mentions in Nov alone)
Food System Focus (+24%): Meat production's climate impact becomes mainstream
EV Reality Check (+22%): From optimism → practical barriers ("too expensive, too heavy")

### 4. Strategic Cultural Interpretations
| Aspect | Korea ESG | UK ESG |
|------|-----------|--------|
| Concept | Corporate Comprehensive Responsibility | Climate Crisis Response Driver |
| Focus | Institutional Standards (K-ESG, GRI) | Regulatory Compliance & Political Activism |
| Trend | Standardization & Certification | Politicization & Personalization |

## Methodology
### Neural Topic Modeling
Model: BERTopic + Multilingual BERT Embeddings
Data Collection:

Period: January 1, 2023 – December 31, 2024
Sources:

UK: The Guardian API (quarterly balanced sampling)
Korea: Major news outlets
Volume: ~40,000 articles per country

Preprocessing Pipeline:
Deduplication: TF-IDF + Cosine Similarity (threshold: 0.8)
Removed 393 duplicate UK articles (1.1%)

Length Filtering:
UK: 400–10,000 characters
Korea: 200–10,000 characters

Content Type: Article-only (excluded liveblogs, interactives)
ESG Classification: Keyword-based scoring + manual validation

UK Environmental: Strict filtering (92.6% → refined to remove non-environmental)
Social & Governance: Rule-based + keyword validation
