# datascience_salary_prediction
This project aimed to predict the salary of Data Scientists in North America, Africa, Asia and Europe
# Comparing & Predicting Data Scientist Salaries Across Continents

## 👤 Author
Ifeoma Mary-Ann James 

## 📌 Project Overview
An end-to-end descriptive and predictive analysis comparing 
annual salaries of Data Scientists across Africa, Asia, 
North America and Europe.

**The core question:**
> "What drives the salary gap between Data Scientists 
> across continents and can we predict it?"

---

## 🗂️ Project Structure

| File | Description |
|---|---|
| `Project_2.ipynb` | Full analysis notebook |
| `salaries.csv` | Raw dataset — 105,434 records |
| `README.md` | Project documentation |

---

## 📊 Dataset

| Property | Details |
|---|---|
| Source | Global Data Science Salaries Dataset |
| Original Records | 105,434 rows |
| After Deduplication | 52,437 rows |
| Target Variable | salary_in_usd |
| Continents | Africa, Asia, North America, Europe |
| Features | work_year, experience_level, employment_type, job_title, salary_currency, remote_ratio, company_size |

---

## 🔍 Key Questions Answered

### Geographic & Distributional
- What is the mean and median salary per continent?
- How does salary variance differ between continents?
- Does North America show wider salary distribution?
- Are there extreme outliers pulling the global average?

### Experience & Demographics
- How does experience level distribution vary by continent?
- Does a Senior Data Scientist in Asia out-earn an Entry-level in North America?
- Where does the salary gap widen or narrow most?

### Employment Structure
- What proportion of African and Asian data scientists work for foreign companies?
- How much more do foreign company employees earn?
- How does company size correlate with salary?
- Does USD payout vs local currency explain salary variance?

---

## 📈 Key Findings

- **North America dominates** highest mean and median salary by a significant margin
- **Geo-arbitrage is real** African and Asian data scientists working for foreign companies earn 50-150% more than local equivalents
- **Senior Asian data scientists do NOT out-earn Entry-level North American counterparts** the geographic premium is that powerful
- **ANOVA confirmed** experience level, region and company size ALL significantly affect salary (p < 0.05)
- **USD payout raises the baseline** even in lower cost-of-living regions, USD-denominated salaries are higher

---

## 🤖 Models Built

| Model | Test R² | RMSE |
|---|---|---|
| Linear Regression | Low | High |
| Ridge Regression | Low | High |
| Lasso Regression | Low | High |
| Decision Tree | Moderate | Moderate |
| Random Forest | Moderate | Moderate |
| **Gradient Boosting (Champion)** | **0.1742 CV** | **Lowest** |

**Champion: Gradient Boosting**
- CV Mean R²: 0.1742
- Marginally outperforms Random Forest (0.1740)
- Salary rankings across regions directionally correct

---

## 💡 Why R² Is Relatively Low

Salary prediction is inherently complex. The 83% unexplained variance reflects:
- Individual negotiation skill
- Company-specific pay bands
- Specific technical skills (Python, PyTorch, Spark)
- Years within each experience tier
- Industry sector variation

Despite this, regional salary rankings are consistent with EDA findings  making the model useful for directional trend analysis.

---

## 🛠️ Tools & Libraries

```python
pandas | numpy | janitor | scikit-learn | 
plotnine | matplotlib | scipy | statsmodels
```

## 🚀 How To Run

1. Clone this repository
2. Install requirements:
```bash
pip install pandas numpy pyjanitor scikit-learn 
            plotnine matplotlib scipy statsmodels
```
3. Add `salaries.csv` to the same folder
4. Open `Project_2.ipynb` and run all cells

---

## 🔗 Connect
- LinkedIn: linkedin.com/in/ifeoma-james-4458321ba
- GitHub: github.com/Ifeoma28
