# Gen Z / Alpha Interest Volatility Analysis
## Which domains shift fastest — and which stay sticky?

A data analysis project examining **10 interest domains** 
across **Gen Z (1997–2012)** and **Gen Alpha (2013–2025)** 
to score, tier and visualise interest volatility.

---

### Real-world question
Which Gen Z and Alpha interest domains shift fast enough 
to demand constant reinvestment — and which are stable 
enough to anchor long-term strategy?

---

### Methodology

| Step | Action |
|---|---|
| 1 | Define real-world question |
| 2 | Identify volatility drivers → dataset columns |
| 3 | Build dataset from literature + public sources |
| 4 | Clean and validate |
| 5 | EDA — 4 natural questions, findings after output |
| 6 | Weighted scoring engine + hard constraints |
| 7 | One insight per chart — 4 charts total |
| 8 | Plain-language conclusions |

---

### Dataset columns

| Column | Measures |
|---|---|
| `trend_cycle_months` | How fast trends die in this domain |
| `platform_dependency` | How tied to one platform (0–10) |
| `identity_attachment` | How tied to self-image (0–10) |
| `identity_type` | achieved vs aspirational |
| `attention_shift_rate` | YoY attention change % |
| `peer_influence_score` | Peer pressure drives adoption (0–10) |

---

### Scoring engine

volatility_score = 0.35 × trend_cycle_inv
+ 0.25 × peer_influence
+ 0.20 × attention_shift
+ 0.20 × platform_dependency

**Hard constraint:** `identity_attachment > 7.0` 
caps score at 0.65 maximum — high identity domains 
cannot be Quicksand regardless of other signals.

### Volatility tiers

| Score | Tier | Meaning |
|---|---|---|
| 0.75–1.0 | 🔴 Quicksand | Constant refresh needed |
| 0.55–0.74 | 🟠 Shifting | Active management needed |
| 0.35–0.54 | 🟡 Stable | Periodic refresh sufficient |
| 0.00–0.34 | 🟢 Evergreen | Long term investment safe |

---

### Key findings

1. **Fashion Gen Alpha is the only Quicksand domain**
2. **Gen Z has zero Quicksand domains** — mid-journey in everything
3. **Mental Health is top priority for both cohorts**
4. **Two types of Evergreen exist** — true (identity-rooted) vs false (not yet engaged)
5. **Gen Alpha is paradoxically more volatile despite stronger self-identity** — aspirational identity shifts with environment

---

### One line summary
> Sell to Gen Z today. Position for Gen Alpha tomorrow.

---

### Data sources
### Data sources

| Domain | Source | Year | URL |
|---|---|---|---|
| Social Media | The List / InVideo — TikTok trend lifespan | 2022 | thelist.com/800454/how-long-does-an-average-tiktok-trend-last |
| Social Media | Pew Research — Teens Social Media & Technology | 2023 | pewresearch.org/internet/2023/12/11/teens-social-media-and-technology-2023 |
| Music | TikTok Billboard Top 50 Chart | 2023 | billboard.com/charts/tiktok-billboard-top-50 |
| Music | Nielsen Music 360 | 2023 | nielsen.com/insights/2023/music-360-2023-highlights |
| Fashion | Edited.com — Gen Z Fashion Trends | 2023 | edited.com/resources/gen-z-fashion-trends |
| Fashion | McKinsey State of Fashion | 2024 | mckinsey.com/industries/retail/our-insights/state-of-fashion |
| Gaming | Deloitte Digital Media Trends | 2024 | deloitte.com/us/en/insights/industry/technology/digital-media-trends |
| Gaming | Newzoo Global Gamer Study | 2023 | newzoo.com/resources/blog/newzoos-global-gamer-study-2023 |
| Mental Health | Annie E. Casey Foundation — Gen Z Mental Health | 2023 | aecf.org/blog/generation-z-and-mental-health |
| Mental Health | Harmony Healthcare IT — Mental Health Statistics | 2025 | harmonyhealthcareit.com/blog/mental-health-statistics |
| Finance | CFA Institute & FINRA — Gen Z Investing | 2023 | rpc.cfainstitute.org/research/reports/2023/gen-z-investing |
| Finance | YouGov — Gen Z Cryptocurrency Ownership | 2025 | business.yougov.com/content/48702-gen-z-investing-crypto |
| Food & Drink | Food & Beverage Magazine — Viral Food Trends | 2024 | fb101.com/why-84-of-gen-z-are-trying-social-media-food-trends |
| Food & Drink | Attest — Gen Z Food Trends | 2023 | askattest.com/blog/research/gen-z-food-trends |
| Sports & Fitness | ABC Fitness Wellness Watch | 2024 | globenewswire.com/news-release/2024/09/18/2948247 |
| Sports & Fitness | Les Mills Global Fitness Report | 2023 | lesmills.com/us/clubs-and-facilities/research-insights/fitness-trends |
| Career | Deloitte Gen Z Survey | 2023 | deloitte.com/global/en/about/press-room/2023-gen-z-and-millenial-survey |
| Career | Handshake Network Trends | 2023 | joinhandshake.com/blog/network-trends/gen-z-mental-health-at-work |
| Activism | United Way NCA Gen Z Activism Survey | 2023 | unitedwaynca.org/blog/gen-z-activism-survey |
| Activism | AEI Survey — Gen Alpha & Progress | 2024 | aei.org/education/gen-alpha-and-the-possibility-of-progress |
---

### Repository structure

genz-interest-volatility/
├── data/
│   └── raw/
│       └── genz_alpha_interests_raw.csv
├── notebooks/
│   └── genz_alpha_analysis.ipynb
├── outputs/
│   └── charts/
│       ├── chart1_heatmap.png
│       ├── chart2_trend_cycle.png
│       ├── chart3_provider_priority.png
│       └── chart4_radar.png
├── .gitignore
└── README.md
___
### Published Work

| Platform | Link |
|---|---|
| Kaggle Notebook | [Gen Z & Alpha Interest Volatility Analysis](https://www.kaggle.com/code/omcaru/gen-z-alpha-interest-volatility-analysis) |
| Kaggle Dataset | [Gen Z Alpha Interest Volatility Dataset](https://www.kaggle.com/datasets/omcaru/gen-z-alpha-interest-volatility-dataset) |
---
*Dataset constructed from literature estimates. 
All values sourced and reasoned from public research 
(2022–2024). See notebook for full source citations.*
