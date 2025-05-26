# Fraud Detection at Contoso Bank: Prioritizing Potential Fraud Cases

## Question
As an analyst in Contoso Bank's Fraud Investigation Team, your tasks are:
1. **Shortlist the top 5 customers who are most likely victims of actual fraud**, based on the data provided.
2. **For each of the top 5 customers, provide a rationale** explaining why they should be prioritized for investigation.
3. **Predict which of the top 5 customers are actual fraud cases**.

**Note:** The number of actual fraud cases in the dataset ranges from **0 to 4**. Your analysis should aim to:
- **Identify true fraud cases** to prevent financial loss.
- **Minimize false positives** to avoid unnecessary customer friction and maintain customer satisfaction.

## Instruction
- Thoroughly analyze the provided datasets to identify patterns and indicators of fraudulent activity.
- Use quantitative analysis and logical reasoning to support your conclusions.
- Include all intermediate calculations and reasoning steps.
- Reference specific data points from the datasets in your rationale.
- Provide a brief **executive summary** at the beginning of your solution, highlighting your key findings and recommendations.
- Present your findings in a clear and concise manner, suitable for presentation to the Fraud Investigation Team.

## Background
Contoso Bank employs advanced fraud detection systems to monitor transactions and identify potential fraudulent activities in real-time. Recently, the bank's systems have flagged **30 customers** for potential fraud. The Fraud Investigation Team needs to prioritize these cases to efficiently allocate resources and minimize customer friction.

Below are datasets collected from various systems, including transaction logs, customer profiles, device usage patterns, and internal compliance reports. The data includes both relevant and additional information to provide a comprehensive view of each customer's activity.

---

### Dataset 1: Customer Transaction Summary

Customer ID Total Transactions Last 24 Hours  Total Amount Last 24 Hours (USD)  Average Transaction Amount (USD)  Flagged Transactions
C001  5 $250  $50 No
C002  50  $10,000 $200  Yes
C003  3 $90 $30 No
C004  4 $400  $100  No
C005  35  $7,000  $200  Yes
C006  6 $600  $100  No
C007  2 $100  $50 No
C008  3 $300  $100  No
C009  7 $700  $100  No
C010  5 $250  $50 No
C011  8 $800  $100  No
C012  6 $300  $50 No
C013  10  $500  $50 No
C014  12  $1,200  $100  No
C015  40  $8,000  $200  Yes
C016  4 $400  $100  No
C017  5 $500  $100  No
C018  3 $300  $100  No
C019  6 $600  $100  No
C020  2 $100  $50 No
C021  3 $150  $50 No
C022  4 $200  $50 No
C023  45  $9,500  $211  Yes
C024  5 $500  $100  No
C025  6 $600  $100  No
C026  7 $700  $100  No
C027  8 $800  $100  No
C028  9 $900  $100  No
C029  2 $200  $100  No
C030  25  $2,500  $100  Yes

### Dataset 2: Fraud Risk Scores

Customer ID Fraud Risk Score (0 - 100)
------------- ----------------------------
C001  20
C002  95
C003  15
C004  40
C005  88
C006  35
C007  25
C008  30
C009  45
C010  50
C011  60
C012  55
C013  40
C014  42
C015  94
C016  35
C017  40
C018  38
C019  42
C020  50
C021  55
C022  60
C023  70
C024  30
C025  35
C026  40
C027  60
C028  65
C029  70
C030  80

### Dataset 3: Customer Profiles

Customer ID Account Age (Years) Account Type  Previous Fraud History  VIP Customer
------------- --------------------- ------------------------  ------------------------  --------------
C001  5 Savings No  No
C002  0.5 Checking  No  No
C003  10  Savings and Checking  Yes Yes
C004  2 Checking  No  No
C005  1 Checking  No  No
C006  3 Savings No  No
C007  7 Savings No  No
C008  8 Savings No  No
C009  2 Checking  No  No
C010  4 Savings No  No
C011  5 Checking  No  No
C012  6 Savings No  No
C013  3 Checking  No  No
C014  2 Savings No  No
C015  1 Savings No  No
C016  2 Checking  No  No
C017  3 Savings No  No
C018  4 Checking  No  No
C019  5 Savings No  No
C020  6 Checking  No  No
C021  3 Savings No  No
C022  2 Checking  No  No
C023  2 Checking  Yes No
C024  3 Savings No  No
C025  4 Checking  No  No
C026  5 Savings No  No
C027  6 Checking  No  No
C028  7 Savings No  No
C029  3 Checking  No  No
C030  3 Savings No  No

### Dataset 4: Device Usage Patterns

Customer ID Registered Devices  New Devices Used Last 24h Suspicious Device Activity
------------- --------------------  --------------------------- ----------------------------
C001  2 0 No
C002  1 5 Yes
C003  3 0 No
C004  2 0 No
C005  2 2 Yes
C006  2 0 No
C007  1 0 No
C008  2 0 No
C009  2 0 No
C010  2 0 No
C011  2 1 No
C012  2 0 No
C013  2 1 No
C014  2 0 No
C015  1 4 Yes
C016  2 0 No
C017  2 0 No
C018  2 0 No
C019  2 0 No
C020  1 0 No
C021  2 1 No
C022  2 0 No
C023  2 3 Yes
C024  2 0 No
C025  2 0 No
C026  2 0 No
C027  2 0 No
C028  2 0 No
C029  2 0 No
C030  2 2 Yes

### Dataset 5: Transaction Location Analysis

Customer ID Home Location Transactions in Last 24h  Locations Used  Unusual Locations
------------- --------------- --------------------------  ----------------- -------------------
C001  City A  City A  1 No
C002  City B  Multiple Cities 5 Yes
C003  City C  City C  1 No
C004  City D  City D  1 No
C005  City E  City E  1 No
C006  City F  City F  1 No
C007  City G  City G  1 No
C008  City H  City H  1 No
C009  City I  City I  1 No
C010  City J  City J  1 No
C011  City K  City K  1 No
C012  City L  City L  1 No
C013  City M  City M  1 No
C014  City N  City N  1 No
C015  City D  Multiple Cities 8 Yes
C016  City O  City O  1 No
C017  City P  City P  1 No
C018  City Q  City Q  1 No
C019  City R  City R  1 No
C020  City S  City S  1 No
C021  City T  City T  1 No
C022  City U  City U  1 No
C023  City E  Multiple Countries  3 Yes
C024  City V  City V  1 No
C025  City W  City W  1 No
C026  City X  City X  1 No
C027  City Y  City Y  1 No
C028  City Z  City Z  1 No
C029  City AA City AA 1 No
C030  City F  City F  1 No

### Dataset 6: Merchant Category Codes (MCC) Analysis

Customer ID Retail  Travel  Electronics Gambling
------------- --------  --------  ------------- ----------
C001  70% 5%  10% 0%
C002  10% 50% 30% 5%
C003  60% 10% 20% 0%
C004  80% 5%  5%  0%
C005  15% 60% 15% 5%
C006  50% 10% 20% 0%
C007  70% 5%  10% 0%
C008  80% 5%  5%  0%
C009  65% 10% 15% 0%
C010  70% 5%  10% 0%
C011  75% 5%  5%  0%
C012  60% 5%  20% 0%
C013  55% 10% 15% 0%
C014  80% 5%  5%  0%
C015  20% 50% 20% 5%
C016  75% 5%  10% 0%
C017  70% 10% 10% 0%
C018  65% 10% 15% 0%
C019  60% 5%  20% 0%
C020  70% 5%  10% 0%
C021  80% 5%  5%  0%
C022  75% 5%  5%  0%
C023  15% 70% 10% 0%
C024  65% 10% 15% 0%
C025  70% 5%  10% 0%
C026  80% 5%  5%  0%
C027  60% 10% 20% 0%
C028  75% 5%  10% 0%
C029  70% 10% 10% 0%
C030  85% 5%  5%  0%

### Dataset 7: Customer Satisfaction Scores

Customer ID Satisfaction Score
------------- --------------------
C001  8.5
C002  6.0
C003  9.0
C004  8.0
C005  6.5
C006  7.5
C007  8.0
C008  8.2
C009  8.3
C010  8.5
C011  7.8
C012  8.1
C013  8.4
C014  8.6
C015  7.0
C016  7.5
C017  8.0
C018  8.2
C019  8.3
C020  8.5
C021  8.7
C022  8.8
C023  6.5
C024  8.2
C025  8.5
C026  8.0
C027  8.2
C028  8.3
C029  8.4
C030  7.5

### Dataset 8: Internal Audit Flags

Customer ID AML Flags KYC Compliance Issues
------------- ----------- -----------------------
C001  No  No
C002  Yes Yes
C003  No  No
C004  No  No
C005  Yes No
C006  No  No
C007  No  No
C008  No  No
C009  Yes  Yes
C010  No  No
C011  No  No
C012  Yes  No
C013  No  No
C014  No  No
C015  Yes No
C016  No  No
C017  No  No
C018  No  Yes
C019  No  No
C020  No  No
C021  Yes  Yes
C022  No  No
C023  Yes Yes
C024  No  No
C025  No  No
C026  No  No
C027  Yes  Yes
C028  No  No
C029  No  No
C030  No  No

### Dataset 9: Recent Customer Communications

Customer ID Contact Reason  Date
------------- --------------------------------- ------------
C001  Account Inquiry 2023-09-15
C002  No Recent Contact N/A
C003  Feedback on Service 2023-09-14
C004  Account Update  2023-09-13
C005  No Recent Contact N/A
C006  Balance Inquiry 2023-09-10
C007  Account Inquiry 2023-09-11
C008  Feedback on Service 2023-09-12
C009  Account Update  2023-09-13
C010  Account Inquiry 2023-09-14
C011  No Recent Contact N/A
C012  Balance Inquiry 2023-09-10
C013  Feedback on Service 2023-09-12
C014  Account Update  2023-09-13
C016  Account Inquiry 2023-09-14
C017  No Recent Contact N/A
C018  Balance Inquiry 2023-09-10
C019  Feedback on Service 2023-09-12
C020  Account Update  2023-09-13
C021  Account Inquiry 2023-09-14
C022  No Recent Contact N/A
C023  No Recent Contact N/A
C024  Balance Inquiry 2023-09-10
C025  Feedback on Service 2023-09-12
C026  Account Update  2023-09-13
C027  Account Inquiry 2023-09-14
C028  No Recent Contact N/A
C029  Balance Inquiry 2023-09-10
C030  Account Inquiry 2023-09-15

### Dataset 10: Social Media Activity

Customer ID Positive Mentions Negative Mentions
------------- ------------------- -------------------
C001  2 0
C002  0 1
C003  1 0
C004  1 0
C005  0 0
C006  1 0
C007  2 0
C008  1 0
C009  0 0
C010  1 0
C011  1 0
C012  1 0
C013  1 0
C014  1 0
C015  0 1
C016  1 0
C017  1 0
C018  1 0
C019  1 0
C020  1 0
C021  1 0
C022  1 0
C023  0 1
C024  1 0
C025  1 0
C026  1 0
C027  1 0
C028  1 0
C029  1 0
C030  1 0

### Dataset 11: Transcripts of Calls Made by the Customers

Call 1: Customer ID C002

Agent: Good morning! Thank you for calling Contoso Bank. How can I assist you today?

C002: Hi, I'm having trouble accessing my online banking account. I think I need to reset my password.

Agent: I can help you with that. For security purposes, I'll need to ask you a few identity verification questions. Can you tell me the name of your first pet?

C002: Oh, I don't remember what I set for that question.

Agent: No worries. Let's try another one. What is the street name where you grew up?

C002: I'm not sure about that one either. Is there another way I can verify my identity?

Agent: I can't authorize you unless you know your identity questions.

Call 2: Customer ID C005

Agent: Thank you for calling Contoso Bank. How may I assist you today?

C005: Hi, I wanted to inquire about updating my mailing address on file.

Agent: Sure, I can help with that. Could you please verify your account number and current address for security purposes?

C005: My account number is 123456789, and my current address is 123 Elm Street.

Agent: Thank you for verifying that information. What is your new address?

C005: It's 789 Oak Avenue.

Agent: Great, I've updated your address. Is there anything else I can help you with today?

C005: Yes, I'd like to register my banking on my new iPhone I've purchased, as well as my new iPad, can I do that?

Agent: You can simply download the app, and use your previous device to help authenticate it as a second factor check. Do you still have your old device?

C005: Yes, I do. Ok that sounds great thanks!

Call 3: Customer ID C006

Agent: Welcome to Contoso Bank. How can I help you today?

C006: Hello, I was wondering if I could get some information about my recent transactions. I think there's a mistake on my account.

Agent: I can assist you with that. Can you please confirm your account number and the specific transaction you're concerned about?

C006: My account number is 987654321, and it's a transaction from last week at GroceryMart.

Agent: Thank you. Let me check... It appears the amount charged was $75. Is that what you're seeing?

C006: Yes, but I only spent $55. Can we dispute this charge?

Agent: Absolutely. I'll initiate a dispute for you. You'll receive updates via email.

Call 4: Customer ID C008

Agent: Thank you for calling Contoso Bank. How may I assist you today?

C008: Hi, I wanted to check the interest rate on my savings account.

Agent: Certainly, could you please verify your account number?

C008: Yes, it's 555111222.

Agent: Thank you. Your current savings account interest rate is 1.5% annually.

C008: Great, thank you for the information. That's all I needed.

Agent: You're welcome! Have a great day.

Call 5: Customer ID C025

Agent: Good day! Thank you for calling Contoso Bank. How can I help you today?

C025: Hi, I need to reset my online banking password. I forgot it.

Agent: No problem. I'll send a verification code to your registered phone number. Could you confirm your number?

C025: Sure, it's 555-1234.

Agent: Thank you. I've sent the code. Please let me know once you receive it.

C025: I got it. The code is 6789.

Agent: Perfect. Your password has been reset. You'll receive an email with further instructions.

Call 6: Customer ID C030

Agent: Welcome to Contoso Bank. How may I help you?

C030: Hi, I received a credit card offer in the mail and wanted to know more about it.

Agent: Certainly! Could you provide me with the offer code mentioned in the letter?

C030: It's 123ABC.

Agent: Thank you. This offer includes a 0% introductory APR for 12 months and no annual fee for the first year.

C030: Sounds good. How do I apply?

Agent: I can help you with the application process over the phone, or you can apply online using the offer code.

C030: I'd like to apply now, please.

Agent: Great, let's get started!

Call 6: Customer ID C015

Agent: Good afternoon! Thank you for calling Contoso Bank. How can I assist you today?

C015: Hi, I'm planning to go on a holiday soon and I'm interested in applying for a travel credit card. Could you tell me more about the options you have?

Agent: Absolutely! We have a couple of great travel credit card options. Are you looking for a card with specific benefits, like no foreign transaction fees or travel rewards?

C015: Yes, I'm particularly interested in a card that offers travel rewards and has no foreign transaction fees.

Agent: In that case, I recommend our Contoso Travel Rewards Card. It offers 2x points on travel and dining, no foreign transaction fees, and a generous sign-up bonus if you spend a certain amount in the first three months.

C015: That sounds perfect. What is the annual fee for this card?

Agent: The annual fee is $95, but it's waived for the first year.

C015: Great! How do I apply for this card?

Agent: I can assist you with the application over the phone, or you can apply online through our website. Which would you prefer?

C015: Let's do it over the phone, please.

Agent: Certainly! I'll just need to gather some information to get started. Do you have a few minutes?

C015: Yes, I'm ready.

Agent: Great, let's begin!

### Dataset 12: Recent Purchases for Customers

Customer ID Item  Price
C002  SIM Card - Brand A  $10.00
C002  SIM Card - Brand B  $12.00
C002  SIM Card - Brand C  $8.00
C002  Old Android Phone Model $50.00
C003  Grocery items - Fresh Produce $30.00
C003  Household Cleaning Supplies $15.00
C003  Coffee Maker  $45.00
C003  Paperback Novel $12.00
C001  Office Supplies - Pens and Notepads $20.00
C001  Streaming Service Subscription  $9.99
C001  Gym Membership Renewal  $50.00
C001  Bluetooth Headphones  $75.00
C005  iPhone 16 XL  $1300.00
C005  iPad 5G  $1100.00
C010  Online Course - Digital Marketing $150.00
C010  Dining Out - Italian Restaurant $40.00
C010  Clothing - Casual T-Shirts  $25.00
C010  Electric Toothbrush $60.00
C015  Flight Ticket - Mexico  $350.00
C015  Flight Ticket - Denver  $200.00
C015  Travel Pillow $15.00
C015  Sleeping Tablets  $10.00
C028  Running Shoes - Brand X $80.00
C028  Yoga Mat  $25.00
C028  Fitness Tracker $99.00
C028  Dumbbells Set $40.00