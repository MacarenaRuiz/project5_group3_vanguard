# Customer Experience (CX) Analysis

**Presented by:**  
Macarena Ruiz, Egbe Grace, Viktoria Gluhovskaya, Marianne Filbig

**The Full presentation:** https://docs.google.com/presentation/d/1Oi1EdEt2b-jIIuWHGRSOk-RvK7pxw20mUzWgaJEXhXc/edit?slide=id.g371532aa70c_3_44#slide=id.g371532aa70c_3_44

# Vanguard Customer Experience (CX) Analysis

## Project Overview
This project focuses on evaluating whether a redesign of Vanguard's User Interface (UI) is justifiable based on improvements in customer experience (CX) metrics such as:
- Completion Rate
- Error Rate
- Time Spent per Process Step

We conducted a thorough A/B test between the **Control** and **Test** groups using real-world user interaction data.

## Business Case: Vanguard Digital Challenge
Vanguard is evaluating a potential UI redesign to make the online process smoother and encourage higher client conversion.

**Key Question:** Is the redesign worth the investment?

**Goals:**
- Improve user experience and process efficiency
- Encourage more users to complete the online process

**Success Threshold:** 5% uplift in Completion Rate

## Data Pipeline & Cleaning Process
- **Loaded Datasets:**
  - df_final_demo (df1)
  - df_final_web_data_pt_1 (df2)
  - df_final_web_data_pt_2 (df3)
  - df_final_experiments_clients (df4)

- **Data Wrangling Steps:**
  - Cleaned column names, removed invalid/duplicate values
  - Merged all dataframes into a single dataset
  - Dropped null values in key variables

## Exploratory Data Analysis (EDA)
- **Gender Distribution:** Nearly equal male-female participation in both Control and Test groups
- **Age Distribution:** The average age of 48 years for Control group and 49 years for Test group corresponds to general client average of 48,5 years of age.  
- **Client Fidelity:** Most users had a tenure between 5 to 15 years
- **Sample Representativity:**
  - Control: 23,526 users
  - Test: 26,961 users
  - No major demographic imbalance across variants: The sample groups are representative of the population.

## Key Findings: Control vs. Test

| Metric            | Control | Test   | Delta (Test - Control) |
|-------------------|---------|--------|-------------------------|
| Completion Rate % | 65.57   | 69.29  | +3.72                   |
| Error Rate %      | 34.42   | 37.82  | +3.40                   |
| Start (sec)       | 62.92   | 60.57  | -2.35                   |
| Step 1 (sec)      | 50.24   | 60.50  | +10.26                  |
| Step 2 (sec)      | 91.59   | 88.59  | -3.00                   |
| Step 3 (sec)      | 135.36  | 128.97 | -6.39                   |
| Confirm (sec)     | 153.03  | 236.24 | +83.21                  |

**Interpretation:**
- ✅ Completion rate improved (+3.72%)
- ✅ Step 2 and Step 3 were faster in the Test version
- ❌ Error rate increased (+3,40%)
- ❌ Step 1 and Confirm screen took significantly longer in the Test group
- ❌ Confirm screen delay (+83.21s) may signal user hesitation or confusion

## Hypothesis Testing
- **Null Hypothesis (H0):** Test group has equal/lower completion rate than Control
- **Alternative Hypothesis (H1):** Test group has a higher completion rate
- **Z-Statistic:** -18.6843
- **P-value:** < 0.0001
- **Result:** Reject the null hypothesis → Completion rate improvement is statistically significant

## Recommendations
Although the Test version shows statistically significant gains, it did **not reach the 5% business threshold** for completion rate improvement. 

- 🔴 Confirm step took much longer → major UX concern
- 🔴 Step 1 slower → possibly due to added fields

**Final Recommendation:**
> Keep the current UI design and instead optimize specific funnel steps where the Test version performed better (Step 2, Step 3).

## Teamwork & Project Management
- ✅ Team collaboration was excellent: mutual support and pace alignment
- 🔍 Main challenge: Statistical interpretation of completion rates and cost-benefit tradeoffs

### Tasks Completed:
- EDA & Cleaning
- KPI Analysis
- Hypothesis Testing
- Tableau Dashboard
- Final Presentation
- README Documentation

---

## Final Conclusion
After a thorough analysis of Vanguard's A/B testing data, our team concludes that the new digital interface does show improvement, particularly in Completion Rate. However, it falls short of the 5% benchmark required to justify a full rollout from a business perspective.

### Verdict:
- The new interface **increases completion rate by +3.72%**.
- **Statistically significant**, but not **operationally sufficient**.

### Our Recommendation:
- Do **not invest** in full-scale redesign yet.
- Instead, **focus efforts on optimizing** specific steps (Step 2 and Step 3) in the current interface using insights from the test variant.
- Improve user flow at **Step 1 and Confirm** page to reduce hesitation and confusion.

## Resources
- Vanguard Corporate Site: https://investor.vanguard.com/corporate-portal
- Vanguard dataframes: df1, df2, df3, df4

### Tools Used
- Trello (Project Management)
- Slack (Communication)
- Tableau (Visualization)
- Python + Jupyter (Analysis)
- Excel (Preprocessing)

