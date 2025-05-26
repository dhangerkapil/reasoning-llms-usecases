# 📘 Credit Risk Assessment – Use Case Overview

## What Is This Use Case About?

This use case helps a bank decide whether to **approve or reject a mortgage loan** application. It uses a **credit risk assessment model** to analyze a customer's financial situation, employment, and the property they want to buy.

The goal is to make smart, data-based decisions that protect the bank while giving customers fair access to loans.

---

## 🔍 Real-Life Scenario

Imagine you're a loan officer at a bank. A customer wants to borrow **$200,000** to buy a house worth **$250,000**. You need to figure out:

- Can they afford it?
- Is the loan safe for the bank?
- Should the loan be approved, rejected, or approved with conditions?

This prompt walks through how to assess that decision using structured data and policy rules.

---

## 🧩 What Information Is Used?

We look at two main types of information:

### 1. **Customer Financial Profile**
- Credit score (How reliable they are with credit)
- Debt-to-income ratio (How much debt they have vs. income)
- Loan-to-value ratio (How big the loan is compared to the house value)
- Employment status (Are they employed full-time, part-time, etc.?)
- Income and savings
- Other debts (e.g., car loans, credit cards)

### 2. **House & Market Information**
- Property value
- Neighborhood safety and school ratings
- Real estate market trends
- Offered interest rate

---

## 🧠 How Does the Decision Work?

### Step 1: **Rate Each Criterion**
Each factor is rated from A (best) to D (riskier). For example:
- A credit score above 700 = A
- Debt-to-income ratio between 30–39% = B
- Employment is full-time and stable = A

### Step 2: **Create a Composite Rating**
Combine all the individual ratings into one string, like `ABACA`.

### Step 3: **Check Bank Policy**
Each composite rating has a defined:
- **Maximum loan amount**
- **Minimum interest rate**

Using `ABACA`, the bank knows how much they can safely lend and the lowest interest rate they can offer.

### Step 4: **Compare With Customer Request**
Check if the customer’s **requested loan** and the **offered interest rate** are within allowed limits.

### Step 5: **Make a Decision**
Based on:
- Their rating
- Their savings and debt
- The condition of the market and property

The bank decides to:
- ✅ Approve the loan
- ⚠️ Approve with conditions (e.g., larger down payment)
- ❌ Reject the loan

---

## 📝 Example

**Customer:**
- Credit Score: 720 → A
- Debt-to-Income: 35% → B
- Loan-to-Value: 80% → C
- Employment: Full-time → A
- Market Trend: Stable → B

**Composite Rating:** `ABACB`

**Policy Table Lookup:**  
`ABACB` allows a max loan of $300,000 and minimum interest rate of 4.25%.

**Customer Request:**  
Loan of $200,000 at 4.00% — **both are within limits**, so the loan may be approved.

---

## 💡 Why This Matters

This use case is important because it:
- Helps banks **avoid risky loans**
- Ensures **fair treatment** of customers
- Makes decisions **consistent and transparent**
- Can be **automated** to save time and reduce errors

---

## 👤 Who Is This For?

- Bank underwriters and analysts
- AI model developers for financial services
- Risk and compliance officers
- Anyone interested in how loan decisions are made using data


