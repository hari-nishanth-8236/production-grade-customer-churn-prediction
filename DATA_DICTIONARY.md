# Data Dictionary

The notebook merges profile and behavior tables on `customer_id`.

| Field | Business meaning | Modeling role |
|---|---|---|
| `customer_id` | Unique customer identifier | Join key and output identifier; excluded as a feature |
| `churn` | Whether the customer churned | Binary target in training data |
| `age` | Customer age | Profile feature |
| `tenure_months` | Months since customer acquisition | Lifecycle feature |
| `purchase_frequency` | Purchase activity measure | Commercial behavior feature |
| `avg_order_value` | Average order value | Commercial behavior feature |
| `total_spend_6m` | Total spend over the last six months | Commercial behavior feature |
| `recency_days` | Days since the last purchase or activity | Inactivity feature |
| `returns_ratio` | Share of purchases returned | Experience and risk feature |
| `email_open_rate` | Email engagement rate | Engagement feature |
| `app_sessions_per_month` | Average monthly app sessions | Engagement feature |
| `support_tickets_6m` | Support tickets in six months | Service-friction feature |
| `campaign_response_rate` | Response rate to campaigns | Engagement feature |
| `customer_satisfaction_score` | Reported satisfaction score | Experience feature |
| `product_categories_used` | Breadth of product-category usage | Relationship-depth feature |
| `gender`, `region` | Customer profile descriptors | Categorical profile features; review for fairness and necessity |
| `income_tier`, `education_level`, `marital_status` | Profile segmentation fields | Categorical profile features; review for fairness and necessity |
| `contract_type` | Customer contract duration/type | Commercial and lifecycle feature |
| `preferred_channel` | Preferred interaction channel | Engagement feature |
| `loyalty_tier` | Loyalty programme tier | Loyalty feature |
| `last_promotion_used` | Most recent promotion type | Offer and engagement feature |
| `payment_method` | Payment method used | Behavioral categorical feature |

The exact dtypes, missingness, and category values are computed by `Code.ipynb` during execution. Values should be validated against the source data dictionary before production use.
