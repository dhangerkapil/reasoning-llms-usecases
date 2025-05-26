# Credit Risk Assessment Prompt

## Purpose
Credit Risk Assessment

## Instructions
1. A bank is considering whether to approve a $200,000 mortgage loan for a customer who wants to buy a house. The bank has the following information about the customer.
2. Review the customer's credit score, debt-to-income ratio, loan-to-value ratio, employment status, income, savings, other debts, and the house information.
3. Assign a rating for each criterion based on the customer and the house information.
4. Combine the ratings for each criterion to form a composite rating.
5. Look up the maximum loan amount and the minimum interest rate for the composite rating in the policy table.
6. Compare the requested loan amount and the offered interest rate with the policy limits.
7. Decide whether to approve or reject the loan application based on the comparison and other factors.
8. If you need to make assumptions, approve or decline the loan and list the conditions that must first be validated before this decision can be made.

## Customer Information
- **Credit score:** 720 (out of 850)
- **Debt-to-income ratio:** 35%
- **Loan-to-value ratio:** 80%
- **Employment status:** Full-time, stable
- **Income:** $60,000 per year
- **Savings:** $10,000
- **Other debts:** $15,000 (car loan and credit cards)

## House Information
- **Appraised value:** $250,000
- **Location:** Suburban, low crime rate, good school district
- **Market trend:** Stable, moderate demand, low inventory
- **Interest rate:** 4% fixed for 30 years

## Credit Risk Assessment Model
The bank uses a credit risk assessment model that assigns a rating from A to D based on the following criteria:

- **Credit score:** A (700 or above), B (650–699), C (600–649), D (below 600)
- **Debt-to-income ratio:** A (below 30%), B (30–39%), C (40–49%), D (50% or above)
- **Loan-to-value ratio:** A (below 70%), B (70–79%), C (80–89%), D (90% or above)
- **Employment status:** A (full-time, stable), B (full-time, variable), C (part-time, stable), D (part-time, variable or unemployed)
- **Market trend:** A (rising, high demand, low inventory), B (stable, moderate demand, low inventory), C (stable, moderate demand, high inventory), D (declining, low demand, high inventory)

The bank also uses a credit risk assessment policy that defines the maximum loan amount and the minimum interest rate for each rating combination, as shown in the table below:

| Rating | Maximum loan amount | Minimum interest rate |
|--------|---------------------|-----------------------|
| AAAAA  | $500,000            | 3.5%                  |
| AAAAB  | $450,000            | 3.75%                 |
| AAAAC  | $400,000            | 4%                    |
| AAAAD  | $350,000            | 4.25%                 |
| AAABA  | $400,000            | 3.75%                 |
| AAABB  | $350,000            | 4%                    |
| AAABC  | $300,000            | 4.25%                 |
| AAABD  | $250,000            | 4.5%                  |
| AAACA  | $350,000            | 4%                    |
| AAACB  | $300,000            | 4.25%                 |
| AAACC  | $250,000            | 4.5%                  |
| AAACD  | $200,000            | 4.75%                 |
| AAADA  | $300,000            | 4.25%                 |
| AAADB  | $250,000            | 4.5%                  |
| AAADC  | $200,000            | 4.75%                 |
| AAADD  | $150,000            | 5%                    |
| ABAAA  | $400,000            | 4%                    |
| ...    | ...                 | ...                   |
| DDDDD  | $50,000             | 6.5%                  |

## Credit Risk Assessment Process
1. **Assign Ratings:**  
   Assign a rating for each criterion based on the customer and the house information.  
   *Example:* The customer’s credit score of 720 corresponds to a rating of A.

2. **Composite Rating:**  
   Combine the ratings for each criterion to form a composite rating.  
   *Example:* Ratings for credit score, debt-to-income ratio, loan-to-value ratio, and employment status are A, B, C, and A respectively; and the house has a rating of B for market trend. Thus, the composite rating is **ABACA**.

3. **Policy Lookup:**  
   Look up the maximum loan amount and the minimum interest rate for the composite rating in the policy table.  
   *Example:* For composite rating ABACA, maximum loan amount is $300,000 and minimum interest rate is 4.25%.

4. **Comparison:**  
   Compare the requested loan amount and the offered interest rate with the policy limits.  
   *Example:* The customer requests $200,000 and the offered rate is 4%, which are both within the policy limits.

5. **Decision:**  
   Decide whether to approve or reject the loan application based on the comparison and other factors (e.g., credit history, savings, and other debts).  
   *Example:* The bank may approve the loan due to good credit history, sufficient savings, manageable debts, and acceptable loan terms. Alternatively, if factors like a high debt-to-income ratio or risky market trends are present, the bank might reject the request or approve it with conditions.