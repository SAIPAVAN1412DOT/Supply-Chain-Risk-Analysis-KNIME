# Supply-Chain-Risk-Analysis-KNIME
Delivery risk analysis of 180,519 supply chain orders using KNIME. Risk classification — Low, Medium, High. Built with DataCo Kaggle dataset.
# Supply Chain Risk Analysis — KNIME

> *"57% of supply chain orders carry medium to high delivery risk. Most organizations don't know this until a plant shuts down."*

---

## Why I Built This

I've spent close to a decade in procurement in process industries. Fertilizer plants don't stop for anything — except when a critical material doesn't arrive on time.

Delivery risk is not an abstract concept for me. It is a phone call at 11pm from a plant manager asking where a compressor seal is.

I wanted to quantify it. Not gut feel. Not experience alone. Data.

---

## What This Is

A delivery risk classification model built in KNIME using the DataCo Smart Supply Chain dataset from Kaggle — 180,519 real supply chain orders across multiple categories, countries, and customer segments.

Every order is scored and classified into Low, Medium, or High delivery risk based on actual vs scheduled delivery performance.

---

## The Workflow — 7 Nodes

| Node | What it does |
|---|---|
| CSV Reader | Loads 180,519 orders, 53 columns |
| Column Filter | Keeps 10 relevant columns |
| Math Formula | Calculates Delay_days = actual − scheduled |
| Rule Engine | Classifies every order — Low / Medium / High Risk |
| GroupBy | Counts orders per risk category |
| Math Formula | Calculates % share of each category |
| Bar Chart | Visualises risk distribution |

---

## Risk Classification Logic

| Delay | Risk Category |
|---|---|
| 0 or negative — on time or early | Low Risk |
| 1 to 2 days late | Medium Risk |
| 3 to 4 days late | High Risk |
| More than 4 days late | Critical Risk |

---

## Results — 180,519 Orders Analysed

| Risk Category | Orders | % of total |
|---|---|---|
| Low Risk | 77,119 | 42.7% |
| Medium Risk | 89,365 | 49.5% |
| High Risk | 14,035 | 7.8% |

**57% of all orders are Medium or High Risk.**

14,000+ orders were delivered significantly late. In a process plant context — each one of those is a potential production disruption.

---

## Screenshots

**Step 1 — CSV Reader — 180,519 rows loaded**
![CSV Reader](screenshots/1%20CSV%20READER.png)

**Step 2 — Column Filter — 10 relevant columns**
![Column Filter](screenshots/2%20column%20filter.png)

**Step 3 — Math Formula — Delay_days calculated**
![Math Formula](screenshots/3%20math%20formula.png)

**Step 4 — Rule Engine — Risk category assigned**
![Rule Engine](screenshots/4%20RULE%20ENGINE.png)

**Step 5 — GroupBy — Orders counted per category**
![GroupBy](screenshots/5%20GROUP%20BY.png)

**Step 6 — Math Formula — Percentages calculated**
![Math Formula %](screenshots/6%20MATH%20FORMULA%20%.png)

**Step 7 — Bar Chart — Risk distribution visualised**
![Bar Chart](screenshots/7%20BAR%20CHART%20VISUALIZATION.png)

---

## What This Means in Procurement

This workflow can be applied to any supply chain dataset — SAP MM export, ERP data, supplier delivery records.

With plant-level data the same workflow answers:
- Which plant has the highest delivery risk?
- Which supplier category is most unreliable?
- Which country of origin carries the most risk?

Add a Row Filter after the Rule Engine and you have a live high-risk supplier watch list — names, categories, delay days, order values.

This is the foundation. The next step is connecting risk scores to demand planning — adjusting safety stock and reorder points based on supplier reliability.

---

## Dataset

DataCo Smart Supply Chain for Big Data Analysis
Source: [Kaggle](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis)

---

## Tech Stack

- KNIME Analytics Platform
- DataCo Supply Chain Dataset — Kaggle
- Nodes: CSV Reader, Column Filter, Math Formula, Rule Engine, GroupBy, Bar Chart

---

## CradleToContract Portfolio

| Repo | What |
|---|---|
| [Should-Cost + TCO](https://github.com/SAIPAVAN1412DOT/Should-Cost-Tool-Process-Industry) | What should it cost? |
| [Environmental EPD](https://github.com/SAIPAVAN1412DOT/Bearing_mock-epd-OpenLCA) | What does it cost the planet? |
| [Social LCA](https://github.com/SAIPAVAN1412DOT/Bearing-Social-LCA-CradleToContract) | What does it cost people? |
| **Supply Chain Risk — KNIME** | Who can I trust to deliver? |
| KNIME Demand Planning + ML | Can I predict and plan better? — coming next |

---

## About

**Sai Pavan**
Deputy Manager — Procurement
Paradeep Phosphates Limited

CPSM® certified | 10 years process industry | SAP MM | KNIME | AI tools | Digital fluency

🔗 [LinkedIn](https://www.linkedin.com/in/sai-pavan-cpsm%C2%AE-7a1806135/)

---

*© 2026 Sai Pavan · Paradeep Phosphates Limited · CradleToContract*
