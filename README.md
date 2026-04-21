# Immigration Patterns and Pressures: A Multivariate Non-Parametric Approach

## 📌 Overview
This project investigates **immigration patterns and pressures** using a set of **non-parametric statistical methods**.  
The goal is to analyze socio-economic, demographic, and political factors that may contribute to emigration ("brain drain") across countries.

## 🎯 Research Questions
- What are the main pressures influencing emigration across countries?
- Do socio-economic inequality, demographic pressures, or governance factors correlate with migration rates?
- Which non-parametric tests are suitable for cross-sectional data in this context?

## 📊 Methods
We use **non-parametric statistical approaches** because the dataset does not necessarily follow normal distributions.

- **Spearman correlation** — rank-based correlation for monotonic relationships  
- **Kendall’s tau** — alternative rank correlation for ordinal/paired data  
- **Kruskal–Wallis test** — non-parametric ANOVA for group comparisons  
- **Wilcoxon rank-sum test** — pairwise group comparisons  

All scripts are written in **R**.

## 📈 Key Results

The analysis reveals statistically significant relationships between Brain Drain and several socio-economic factors:

* **Economic Inequality:** Spearman ρ = 0.55 (p < 0.001) → moderate positive correlation
* **Demographic Pressures:** Spearman ρ = 0.60 (p < 0.001) → strong positive correlation
* **Human Rights:** Kendall τ = 0.253 (p < 0.001) → weak but significant relationship

Group-based analysis also shows:

* **Public Services:** Significant differences across groups (Kruskal–Wallis χ² ≈ 75, p < 0.001)
* **External Intervention:** Significant difference between groups (Wilcoxon test, p < 0.001)

👉 Overall, countries with higher inequality, demographic pressure, and weaker governance tend to experience higher levels of emigration (brain drain).

## 📊 Figure Interpretation

The generated plots illustrate the statistical relationships:

* **Scatter plots** (Economic Inequality & Demographic Pressure) show clear upward trends → higher values correspond to higher Brain Drain
* **Boxplots** (Public Services & External Intervention) show clear differences between groups
* **Human Rights plot** shows a weaker but still positive relationship

These visual patterns support the statistical test results and confirm consistent relationships across countries.

## 📂 Repository Structure
├── data/ # Raw and sample datasets
│ ├── Immigration_Data.xlsx
│ └── sample.csv
├── scripts/ # R scripts for analysis
│ └── analysis.R
├── output/ # Generated results
│ ├── figures/ # Plots and visualizations
│ └── tables/ # Summary tables and CSV results
├── Poster/ # Project poster (PowerPoint / PDF)
│ └── immigration_poster.pptx
├── proposal.pdf # Research proposal
├── README.md # Project documentation
└── .gitignore # Ignore unnecessary files

## ▶️ How to Run
1. Install R (≥ 4.3.0)  
2. Install required packages:
   ```r
   install.packages(c(
     "tidyverse", "readxl", "ggplot2", "corrplot", 
     "psych", "rstatix", "ggpubr"
   ))
2.Run the analysis:

Rscript scripts/analysis.R


3.Results will be saved in:

output/figures/

output/tables/

4.📈 Example Outputs

Correlation heatmaps (Spearman/Kendall)

Boxplots of emigration pressures by region

Non-parametric test results (p-values in tables)

(Insert screenshots of a plot or two here for better presentation.)

5.📜 License

Code: MIT License

Poster & Documentation: CC-BY 4.0
6.Citation

If you use this project, please cite it as:

@misc{emadi2025immigration,
  author = {Romina Emadi},
  title  = {Immigration Patterns and Pressures: A Multivariate Non-Parametric Approach},
  year   = {2025},
  url    = {https://github.com/Romina7394/Immigration-Patterns-and-Pressures-A-Multivariate-Non-Parametric-Approach}
}

---
📜 License

MIT License (see the LICENSE file).

## 📄 `.gitignore`

```gitignore
# R session files
.Rhistory
.RData
.Ruserdata
.Rproj.user/
*.Rproj

# Temporary files
*.tmp
*.log

# Output artifacts (optional, keep if you don't want to push figures/tables)
output/figures/*
output/tables/*

# OS-specific
.DS_Store
Thumbs.db
