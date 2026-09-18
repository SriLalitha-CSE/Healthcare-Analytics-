# Healthcare Analytics 

## 📌 Overview

This project analyzes household health survey data to understand what drives doctor visit frequency. It examines demographic factors (age, gender, income), health-status indicators (illness episodes, reduced-activity days, general health score, chronic conditions), and access factors (private insurance, free government health cover) to identify statistically significant patterns in healthcare utilization.

## 📊 Dataset

- **5,190 individual records** from a household health survey
- File: `doctor_visits_dataset.csv`

| Column | Description |
|---|---|
| `visits` | Number of doctor consultations in the past 2 weeks |
| `gender` | Male / Female |
| `age` | Age in years (stored as age/100 in the raw file) |
| `income` | Annual income (stored in tens of thousands, raw file) |
| `illness` | Number of illnesses in the past 2 weeks (0-5) |
| `reduced` | Number of days of reduced activity due to illness/injury |
| `health` | General health questionnaire score (0 = best, 12 = worst) |
| `private` | Has private health insurance (yes/no) |
| `freepoor` | Free government health cover due to low income (yes/no) |
| `freerepat` | Free government health cover due to age/disability/veteran status (yes/no) |
| `nchronic` | Chronic condition that does NOT limit activity (yes/no) |
| `lchronic` | Chronic condition that DOES limit activity (yes/no) |

## 🎯 Objectives

- Clean and prepare the survey dataset
- Examine how doctor visits vary by demographic factors (age, gender, income)
- Investigate the relationship between health indicators and doctor visits
- Examine the effect of insurance/health-cover type on utilization
- Apply statistical tests (Pearson correlation, Mann-Whitney U) to confirm significance
- Derive evidence-based insights and recommendations for healthcare planning

## 🛠️ Technology Used

| Tool | Purpose |
|---|---|
| Python | Core programming language |
| Pandas & NumPy | Data cleaning, feature engineering, numerical computation |
| Matplotlib & Seaborn | Statistical charts, distributions, correlation heatmaps |
| SciPy | Pearson correlation and Mann-Whitney U significance testing |
| Jupyter Notebook | End-to-end documentation of the analysis |

## 📁 Repository Structure

```
├── README.md
├── Healthcare_Analytics_for_Doctor_Visits.ipynb        # Full analysis notebook
├── doctor_visits_dataset.csv                            # Raw dataset
└── Healthcare_Analytics_for_Doctor_Visits_Presentation.pptx   # Project presentation slides
```

## 🔑 Key Findings

- Only **20.2%** of people in the sample had at least one doctor visit in the 2-week survey window; visit counts are highly right-skewed.
- **Reduced-activity days (r = 0.42)** and **illness count (r = 0.22)** are the strongest predictors of doctor visits — health need drives utilization more than any other factor.
- People with a **limiting chronic condition** average **3x** the visits of those with no chronic condition (0.60 vs 0.19 visits).
- **Income shows a weak relationship** with visits (r = -0.08), suggesting healthcare-seeking behavior is driven by need rather than ability to pay — consistent with free government cover for eligible groups.
- **65.3%** of people with 3+ illnesses had **zero** doctor visits — a potential access gap worth further investigation.
- Gender and insurance/cover-type differences in visit frequency are statistically significant (p < 0.05).

## 🚀 How to Run

1. Clone this repository
   ```bash
   git clone <your-repo-url>
   cd <repo-folder>
   ```
2. Install dependencies
   ```bash
   pip install pandas numpy matplotlib seaborn scipy jupyter
   ```
3. Launch the notebook
   ```bash
   jupyter notebook Healthcare_Analytics_for_Doctor_Visits.ipynb
   ```
4. Run all cells to reproduce the analysis (the dataset CSV must be in the same folder).

## 📈 Recommendations

- Prioritize outreach to people with multiple illnesses but no recent doctor visit
- Focus preventive care resources on people with limiting chronic conditions
- Monitor gender-based differences in healthcare-seeking behavior
- Continue supporting free government health cover for low-income and eligible groups
- Extend the analysis with longitudinal or larger-scale survey data

## 👤 Author

- **Name:PURRU SRILALITHA SAI PRASANNA**
- **Program:** VOIS AICTE Data Analytics Internship
