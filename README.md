# Drug Safety Hypothesis Testing

## Project Overview

This project uses statistical hypothesis testing to investigate adverse effects reported during a randomized controlled drug trial. Using Python, I compare a drug treatment group with a placebo group to explore whether observed differences in adverse effects and participant ages are statistically significant.

The project uses a modified drug safety dataset originally obtained from Hbiostat, courtesy of the Vanderbilt University Department of Biostatistics.

## Objectives

- Compare the proportion of participants experiencing adverse effects in the drug and placebo groups.
- Test whether the number of adverse effects is associated with treatment group.
- Evaluate whether participant ages differ between the drug and placebo groups.
- Visualize adverse effect counts and age distributions by treatment group.
- Practice statistical inference and exploratory data analysis using Python.

## Tools and Technologies

- **Python** — statistical analysis and data manipulation
- **pandas** — data loading and transformation
- **NumPy** — numerical calculations
- **SciPy** — statistical hypothesis testing
- **statsmodels** — two-sample proportion z-test
- **Pingouin** — chi-square independence analysis
- **Seaborn and Matplotlib** — data visualization

## Dataset

The dataset, `drug_safety.csv`, contains 16,103 observations and eight original columns:

| Column | Description |
|---|---|
| `age` | Participant age |
| `sex` | Participant sex |
| `trx` | Treatment group: Drug or Placebo |
| `week` | Week of testing |
| `wbc` | White blood cell count |
| `rbc` | Red blood cell count |
| `adverse_effects` | Whether at least one adverse effect was recorded |
| `num_effects` | Number of adverse effects experienced |

The dataset contains missing values in the WBC and RBC measurements.

## Methodology

### 1. Data Exploration

Loaded the dataset using pandas and examined its structure, descriptive statistics, sample records, and missing values.

### 2. Proportion of Participants Experiencing Adverse Effects

Applied a two-sample proportion z-test to compare the proportion of observations with adverse effects between the drug and placebo groups.

A count plot was also created to visualize adverse effect counts by treatment group.

### 3. Number of Adverse Effects

Used a chi-square test of independence to examine the relationship between treatment group and the number of adverse effects recorded. Pingouin was also used to explore chi-square test results.

### 4. Age Differences Between Groups

Applied the Mann–Whitney U test to compare participant ages between the drug and placebo groups.

Created age categories and a count plot to visualize the age distribution across treatment groups.

## Results and Key Findings

### Adverse Effect Proportions

- Two-sample proportion z-test p-value: **0.9639**
- Significance level: 0.10
- Conclusion: Failed to reject the null hypothesis. The analysis did not find a statistically significant difference in the proportion of observations with adverse effects between the groups.

### Number of Adverse Effects

- Chi-square statistic: **1.7996**
- Degrees of freedom: 3
- P-value: **0.6150**
- Conclusion: Failed to reject the null hypothesis of independence. The analysis did not find a statistically significant association between treatment group and the number of adverse effects recorded.

### Participant Age Differences

- Mann–Whitney U statistic: **29,149,339.5**
- P-value: **0.2570**
- Significance level: 0.05
- Conclusion: Failed to reject the null hypothesis. The analysis did not find a statistically significant difference in the age distributions of the drug and placebo groups.

## Visualizations

The notebook includes:

- A count plot of adverse effects by treatment group.
- A count plot comparing age categories across drug and placebo groups.

These visualizations complement the statistical tests by making group distributions easier to examine.

## Skills Demonstrated

- Data inspection and missing-value assessment
- Data manipulation using pandas and NumPy
- Statistical hypothesis testing
- Two-sample proportion z-tests
- Chi-square tests of independence
- Mann–Whitney U tests
- Categorical data analysis
- Data visualization using Seaborn and Matplotlib
- Interpreting p-values and statistical significance

## Limitations

The results do not establish that the drug is safe or that the treatment groups are equivalent. Failure to reject a null hypothesis does not prove that no difference exists.

The analysis is limited to the available dataset and the variables examined. Further investigation would be needed to assess individual adverse effects, clinical significance, statistical power, and other safety outcomes.

## Conclusion

This project demonstrates how statistical testing can be used to investigate potential differences in adverse effects and participant characteristics between drug and placebo groups.

The tests performed did not identify statistically significant differences at their selected significance levels. These findings illustrate the role of hypothesis testing in data-driven drug safety investigations, while highlighting the importance of interpreting statistical results in their proper context.

## Data Source

The original dataset is available through [Hbiostat — Vanderbilt University Department of Biostatistics](https://hbiostat.org/data/repo/safety.rda).

The notebook uses a modified version of the original dataset.


