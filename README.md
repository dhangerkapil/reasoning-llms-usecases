# Reasoning Use Case Examples

This repository contains a collection of use case examples demonstrating reasoning capabilities with large language models (LLMs) like O1. Each use case is designed to evaluate interpretable reasoning, dataset referencing, and audit-friendly outputs in financial and insurance domains.

## Use Cases

### 📘 [Auto Insurance Risk Evaluation](./risk-assessment-for-underwriting-health-auto-life-property/README.md)
Evaluates an auto insurance application using datasets like telematics, driving history, and vehicle maintenance logs. Emphasizes traceable, compliance-ready risk classification and justifies premium adjustments.

### 📘 [Cross-Asset Volatility and Sentiment Forecasting](./market-sentiment-and-volatility-forecasting/README.md)
Forecasts 30-day volatility across equities, bonds, and commodities using sentiment data, macroeconomic indicators, and option term structures. Ideal for showcasing O1’s dataset traceability and structured forecasting.

### 📘 [Insurance Claims Processing](./insurance-claims-processing/README.md)
Assesses a property claim for water damage and mold under specific coverage clauses. The use case highlights O1’s step-by-step analysis, regulatory interpretation, and payout calculation logic.

### 📘 [Comprehensive Insurance Coverage Analysis](./insurance-plan/README.md)
Recommends core and add-on coverages for a small business using datasets on risks, incidents, state laws, and benchmark premiums. Showcases O1's structured evaluation of commercial risk and compliance.

### 📘 [Loan Agreement Risk Assessment](./loan-agreement/README.md)
Performs legal risk assessment on a scanned loan contract with degraded footnotes. Focuses on clause-level interpretation, compliance flags, and legal reasoning, emphasizing O1’s strength in ambiguous data environments.

### 📘 [Global Multi-Asset Portfolio Optimization](./portfolio-optimization/README.md)
Optimizes asset allocation across a diversified global portfolio while meeting regulatory risk limits. Highlights O1’s ability to handle high-dimensional financial datasets and justify recommendations using correlations and constraints.

### 📘 [Commercial Insurance Underwriting](./underwriting-analysis/README.md)
Conducts risk-adjusted premium analysis using historical claims, inspection reports, and compliance data. Illustrates O1’s strength in synthesizing multi-source data for commercial insurance underwriting.

### 📘 [Personalized Banking Insights for Client Retention](./customer-relationship-management/README.md)
Analyzes behavior, transaction patterns, and customer feedback to recommend tailored banking services. Demonstrates O1’s ability to distill actionable client insights from structured and semi-structured financial datasets.

### 📘 [Credit Risk Assessment and Management](./credit-risk-assessment-and-management/README.md)
Assesses borrower creditworthiness using repayment history, credit scores, and regulatory thresholds. Highlights O1’s strength in transparent scoring, compliance flagging, and precise lending classification.

### 📘 [Fraud Detection and Compliance Triggers](./fraud-detection-and-prevention/README.md)
Uses behavioral anomalies, transaction metadata, and rule-based compliance filters to flag potential fraud cases. Designed to demonstrate O1’s interpretability in high-stakes forensic audits and compliance workflows.




# Executing the notebook to compare model outputs

To run the notebook, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/dhangerkapil/reasoning-llms-usecases-fsi.git
    cd reasoning-llms-usecases-fsi
    ```

2. Create and activate a virtual environment:
    ```sh
    # For Linux/macOS:
    python3 -m venv venv
    source venv/bin/activate

    # For Windows:
    python -m venv venv
    .\venv\Scripts\activate
    ```

3. Install the required dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Copy the `env_sample` file to `.env` and add your Azure OpenAI endpoint and API key:
    ```sh
    cp env_sample .env
    ```

    Edit the `.env` file to add your Azure OpenAI endpoint and API key:
    ```plaintext
    AZURE_OPENAI_ENDPOINT=your_endpoint
    AZURE_OPENAI_API_KEY=your_api_key
    ```

5. Follow the instructions in the notebook to execute the cells and observe the results.
