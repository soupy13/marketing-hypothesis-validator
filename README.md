# 📊 Marketing A/B Testing Analysis

## ✨ Project Overview
This project evaluates the performance of a digital marketing campaign using statistical hypothesis testing. By comparing conversion rates between a treatment group exposed to advertisements and a control group shown Public Service Announcements (PSAs), this analysis identifies the true impact of the marketing spend. 

## ✨ Dataset
*   **Source File:** `marketing_AB.csv`
*   **Volume:** 588,101 user interactions.
*   **Key Features:**
    *   `test group`: Categorizes users into the 'ad' (treatment) or 'psa' (control) cohorts.
    *   `converted`: Binary indicator showing if a user successfully converted (0 or 1).
    *   `total ads`: The cumulative number of advertisements seen by the user.
    *   `most ads day`: The specific day of the week with the highest ad exposure for the user.
    *   `most ads hour`: The hour of the day with the highest ad exposure.

## ✨ Methodology
The analysis applies rigorous statistical methods to validate the campaign's success:
*   **Independent T-Test (A/B Test):** Used to determine if the difference in conversion rates between the treatment and control groups is statistically significant.
*   **Analysis of Variance (ANOVA):** Applied to evaluate whether the day of the week or the time of day has a statistically significant effect on user conversion.

## ✨ Key Findings & Recommendations
*   **Campaign Lift:** The marketing advertisements drive a significantly higher conversion rate compared to the control group (t-statistic: 7.37, p-value: 1.70e-13).
*   **Behavioral Patterns:** 
    *   Conversions are heavily influenced by the day of the week users see the most ads (ANOVA p-value: 1.80e-85).
    *   The time of day also plays a critical role in driving successful conversions (ANOVA p-value: 7.48e-77).
*   **Business Action:** The marketing team should optimize ad frequency and target users during the identified peak conversion hours and days to maximize return on investment.

## 🛠️ Tech Stack
*   **Data Processing & Statistics:** `pandas`, `scipy`
*   **Visualization:** `matplotlib`, `seaborn`
*   **Modeling & Deployment Frameworks:** `scikit-learn`, `tensorflow`, `gunicorn`

## Getting Started

### Prerequisites
Clone this repository and install the required packages: `requirement.txt`

Running the Analysis:
Ensure the marketing_AB.csv dataset is placed in the /content/ directory, or update the file path directly in the notebook.

Launch the Jupyter environment and run the notebook to execute the statistical tests and generate the conversion rate visualizations.

## 📂 Project Structure
```text
marketing-hypothesis-validator/
│
├── data/
│   └── marketing_AB.csv                # The dataset containing user ad interactions
│
├── notebooks/
│   └── marketing_A_B_Testing.ipynb     # Jupyter notebook with EDA and statistical tests
│
├── requirements.txt                    # Project dependencies (pandas, scipy, etc.)
└── README.md                           # Project documentation
