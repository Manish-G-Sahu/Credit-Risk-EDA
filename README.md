# Credit-Risk-EDA :

## Business Understanding
Consumer finance companies face challenges in lending due to applicants with insufficient credit histories, leading to potential defaults. The goal is to analyze loan application data to identify patterns that can help predict the likelihood of loan repayment. 

- Two primary risks affect loan decisions:
1. Rejecting creditworthy applicants may lead to missed business opportunities.
2. Approving applicants who are likely to default results in financial losses.

The dataset includes scenarios where clients either struggle with payments (delayed beyond a threshold) or meet payment timelines. Loan applications fall into four categories:
- **Approved:** Loan application is accepted.
- **Cancelled:** Client withdraws application mid-process, often due to high risk or poor loan terms.
- **Refused:** Loan application is rejected based on eligibility criteria.
- **Unused offer:** Client cancels the loan at a later stage.

Using EDA, the aim is to understand how consumer and loan characteristics correlate with default tendencies, ensuring only creditworthy applicants are approved.

## Business Objectives
This case study aims to identify patterns which indicate if a client has difficulty paying their instalments which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. This will ensure that the consumers capable of repaying the loan are not rejected. Identification of such applicants using EDA is the aim of this case study.

In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default.  The company can utilise this knowledge for its portfolio and risk assessment.

## Solution :-
📊 **Data Cleaning**:
- In this project, I worked with a dataset containing customer purchase records. The first step was to handle **missing values** in columns like `Age`,'gender' and `Income` by using mean imputation and median-based methods.
- I also identified and removed **outliers** in the `Spending Score` column, which were skewing the data, and replaced them using the interquartile range (IQR) method to make the dataset more reliable.

📈 **Descriptive Statistics**:
- For **distribution analysis**, I visualized `Age`, `Annual Income`, and `Spending Score` using histograms to understand data skewness. I found that **Age** was fairly normally distributed, while **Income** showed a right skew.
- I used **scatter plots** and **pair plots** to analyze correlations between `Income` and `Spending Score` to see if higher incomes led to increased spending, which provided some intriguing insights.

🧩 **Feature Engineering**:
- I created a new feature called `Income_per_Age`, which highlighted income adjusted by age. This feature helped me segment customers based on their purchasing power relative to their age group.
- Additionally, I binned `Age` and `Income` into categorical segments (e.g., Age Groups and Income Tiers) for easier visualization and targeted analysis.

💡 **Insights & Hypotheses**:
- One interesting insight was that **customers in the 30-40 age range with medium-to-high income** showed a significantly higher spending score. This group may be more likely to spend on luxury items, which could help the marketing team with targeted campaigns.
- I also hypothesized that certain customer demographics might prefer specific products. This was supported by a clustering analysis on the spending data, revealing distinct customer segments.


