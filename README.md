# China's Place in Liberal Internationalism
This project analyzes China’s voting behavior in the United Nations Security Council (UNSC) using descriptive statistics and a logistic regression model in R. I answer the question of how liberal China is internationally, as well as the question of whether China's support for a UNSC sanction is a significant determinant of UNSC sanction success.


## Research Questions
1. To what extent does China behave as a liberal actor in the United Nations Security Council (UNSC)?
2. Is China’s support for a UNSC sanction a statistically-significant determinant of sanction success?


## Methods
This project uses descriptive statistics and logistic regression analysis to evaluate China’s voting behavior and its impact on sanction outcomes.
* Unit of analysis: UNSC sanction resolutions
* Dependent variable: Sanction success (binary)
* Independent variable: China’s vote (support vs. non-support, binary)
* Model type: Logistic regression

All analysis was conducted in R.


## Datasets
This project integrates multiple international sanctions and voting datasets:
* China TIES: Contains data on Chinese economic sanctions from 1949–2020 (DOI: 10.1177/07388942241248274)
* EUSANCT: Covers post-Cold War sanctions imposed by the EU, UN, and US (DOI: 10.1177/0738894220948729)
* CR-UNSC: Provides a corpus of UN Security Council resolutions (DOI: 10.5281/zenodo.11212056)
* DPPA-SCVETOES: Contains data on veto usage in the Security Council (https://psdata.un.org/dataset/DPPASCVETOES)


## R Packages Used
1. data.table
2. ggraph
3. gt
4. igraph
5. pscl
6. readxl
7. tidyverse


## Repository Structure
* UNSC_sanctions.qmd (Quarto Source file)
* * UNSC_sanctions.html (Rendered output)


## How to Reproduce
1. Install required packages:

```r
install.packages(c(
  "data.table",
  "ggraph",
  "gt",
  "igraph",
  "pscl",
  "readxl",
  "tidyverse"
))
```

2. Download datasets (see links above)
3. Use with Quarto Document "UNSC_sanctions.qmd"

## Key Findings
China is a liberal actor within the UNSC. China’s voting behavior in the UNSC aligns closely with that of the United States, the United Kingdom, and France. China’s support significantly increases the probability of UNSC sanction success, although there are many other factors important in explaining UNSC sanction success. China does not veto often, it has only vetoed 19 times from 1972-2024. When it does, its vetoes are always against the wishes of the US, the UK, and France. China vetoed sanctions over Syria most often.

## Notes
* I used R version 2025.09.2+418
* I used a network analysis using ggraph to visualize the voting similarity between nations
