# Credit-Risk-EDA :

## Business Understanding
The loan providing companies find it hard to give loans to the people due to their insufficient or non-existent credit history. Because of that, some consumers use it to their advantage by becoming a defaulter. Suppose you work for a consumer finance company which specialises in lending various types of loans to urban customers. You have to use EDA to analyse the patterns present in the data. This will ensure that the applicants capable of repaying the loan are not rejected.

When the company receives a loan application, the company has to decide for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:
If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company.

The data given below contains the information about the loan application at the time of applying for the loan. It contains two types of scenarios:
The client with payment difficulties: he/she had late payment more than X days on at least one of the first Y instalments of the loan in our sample,
All other cases: All other cases when the payment is paid on time.

When a client applies for a loan, there are four types of decisions that could be taken by the client/company):
Approved: The Company has approved loan Application
Cancelled: The client cancelled the application sometime during approval. Either the client changed her/his mind about the loan or in some cases due to a higher risk of the client, he received worse pricing which he did not want.
Refused: The company had rejected the loan (because the client does not meet their requirements etc.).
Unused offer:  Loan has been cancelled by the client but at different stages of the process.
In this case study, you will use EDA to understand how consumer attributes and loan attributes influence the tendency to default.

## Business Objectives
This case study aims to identify patterns which indicate if a client has difficulty paying their instalments which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. This will ensure that the consumers capable of repaying the loan are not rejected. Identification of such applicants using EDA is the aim of this case study.

In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default.  The company can utilise this knowledge for its portfolio and risk assessment.
To develop your understanding of the domain, you are advised to independently research a little about risk analytics - understanding the types of variables and their significance should be enough.

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


