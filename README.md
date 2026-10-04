# ontario-eqao-math-achievement-analysis
# Ontario EQAO Elementary Math Achievement Analysis

## Project Overview
This project examines systemic patterns in Ontario elementary mathematics achievement using open data from the Education Quality and Accountability Office (EQAO). The analysis explores performance distributions across student gender cohorts, school language systems (English vs. French), and school governance models (Public vs. Catholic), evaluating both distributional equity and rates of meeting the provincial standard (Level 3 and Level 4).

---

## Data Source & Methodology
* **Source:** Education Quality and Accountability Office (EQAO) / Ontario Ministry of Education Open Data.
* **Dataset Scope:** School-level assessment records for Elementary Mathematics (Grades 3 and 6).
* **Data Integrity & Governance:**
  * **Level of Analysis:** Filtered strictly to school records (`OrgType == 'S'`), excluding board-level (`'B'`) and provincial aggregate (`'P'`) rows to eliminate double-counting.
  * **Privacy Suppression:** Filtered to unsuppressed records (`Suppressed == 0`) to omit small-cohort cells masked for student privacy compliance.
  * **Sectors Analyzed:** Focused on publicly funded institutions (`FundingType == 1`), segmented into Public and Catholic district school boards via `BoardName`. Provincial specialized schools (`FundingType == 3`, $n = 8$) and private records were excluded from comparative baseline benchmarks.
  * **Effective Sample Size:** $n = 3,255$ validated elementary schools across Ontario.

---

## Executive Summary & Key Findings

### 1. Gender Disparities in Math Performance
* **Provincial Benchmark ($\ge$ Level 3):**
  * **Male Cohort:** **56.9%** met or exceeded the provincial standard (45.1% Level 3; 11.8% Level 4).
  * **Female Cohort:** **48.4%** met or exceeded the provincial standard (40.9% Level 3; 7.5% Level 4).
  * **The Gender Gap:** Male students hold an **8.5 percentage point advantage** overall. This difference is most pronounced at the highest mastery tier (Level 4), where male achievement exceeds female achievement by a ratio of roughly 1.6 to 1 (11.8% vs. 7.5%).
* **Concentration at Level 2 ("Approaching Standard"):**
  * Female students are heavily clustered at **Level 2 (44.3%)**, compared to 37.0% for male students.
  * Severe underperformance rates remain low and nearly identical between cohorts: **7.1%** of female students scored at Level 1 or below (NE1), compared to **6.1%** of male students.

### 2. School System Language & Governance Dynamics
Achievement rates meeting or exceeding the provincial benchmark (Level 3 & Level 4) break down across the four publicly funded sectors as follows:

| System Language | Governance Model | Met Provincial Standard (Levels 3 & 4) |
| :--- | :--- | :---: |
| **French** | **Public** | **65.93%** |
| **French** | **Catholic** | **62.22%** |
| **English** | **Public** | **52.25%** |
| **English** | **Catholic** | **51.22%** |

* **Linguistic Advantage:** Students enrolled in the French-language system outperform their English-system peers by **11 to 14 percentage points** across both governance models.
* **Governance Model Effect:** Public school boards slightly lead Catholic school boards across both language streams (+1.03 percentage points in English; +3.71 percentage points in French).
* **Relative Equity in English Boards:** Performance across English Public (52.25%) and English Catholic (51.22%) boards shows near parity, pointing to consistent system-wide baseline achievement across English-language sectors.
