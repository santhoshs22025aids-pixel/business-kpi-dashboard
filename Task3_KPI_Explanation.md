# Task 3 — Business KPI Dashboard

## Objective
Turn the cleaned synthetic customer churn data into decision-ready metrics and readable visualizations.

## KPI definitions
- **Churn rate:** churned customers / all customers.
- **Retention rate:** customers who did not churn / all customers (equivalently 1 − churn rate).
- **Monthly revenue at risk:** sum of monthly charges for customers marked as churned. This is a proxy for monthly recurring revenue at risk, not a prediction of future losses.
- **Average tenure:** average number of months since signup.

## Verified overall metrics
- Customers: 15
- Churned customers: 7
- Churn rate: 46.7%
- Retention rate: 53.3%
- Monthly revenue at risk: INR 409.93
- Average tenure: 18.8 months

## Segment findings
### Contract type
                customers  churned  churn_rate
ContractType                                  
Month-to-Month          7        7         1.0
One Year                4        0         0.0
Two Year                4        0         0.0
### Subscription type
                  customers  churned  churn_rate
SubscriptionType                                
Basic                     7        5    0.714286
Enterprise                4        0    0.000000
Pro                       4        2    0.500000
### Payment method
               customers  churned  churn_rate
PaymentMethod                                
Bank Transfer          3        0    0.000000
Credit Card            6        2    0.333333
Debit Card             2        2    1.000000
UPI                    4        3    0.750000

## Recommendation
Review Month-to-Month customers first, and investigate Basic-tier customers with multiple support tickets. The sample shows elevated churn in these groups, but the data is synthetic and small. This is a prioritization hypothesis, not causal evidence. Pilot a retention check-in and compare subsequent churn, support-ticket volume, and retention cost against an appropriate comparison group.

## Dashboard usage
Open `Business_KPI_Dashboard.xlsx` and use the dropdowns in the Dashboard sheet for Contract Type, Payment Method, and Tenure Band. KPI cards respond to the filters. Segment Analysis includes segment tables and charts.

## Limitations
The dataset contains only 15 synthetic records. Segment percentages are unstable, and the dashboard is descriptive rather than predictive.
