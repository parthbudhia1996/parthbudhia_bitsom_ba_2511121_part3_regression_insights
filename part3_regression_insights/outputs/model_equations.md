# Mathematical Regression Formulations & Encoding Framework

## Simple Regression Models
### Model 1: Marketing Expenditures Focus
`monthly_sales` = 567,463.56 + 2.05 * `marketing_spend`
* **Coefficient Interpretation:** In isolation, each additional dollar injected into targeted marketing campaigns is associated with an immediate **$2.05** increase in monthly sales.

### Model 2: Footfall Volume Focus
`monthly_sales` = 447,699.03 + 35.64 * `footfall`
* **Coefficient Interpretation:** In isolation, every single additional consumer walking onto a store floor is associated with an average revenue lift of **$35.64**.

---

## Final Selected Multiple Linear Regression Model

**Categorical Variables:** `store_type` (Converted to Dummified indicators)

**Dummy Variables:** `store_type_Mall`, `store_type_High_Street`, `store_type_Residential`

`monthly_sales` = 163,378.75 + 1.17 `marketing_spend` + 33.60 `footfall` + 2,876.51 `inventory_availability_pct` - 11,351.01 `store_type_Mall` - 22,750.66 `store_type_High_Street` - 37,246.11 `store_type_Residential`

### Categorical Variable Dummy Strategy & Reference Baseline
To process qualitative storefront settings in our quantitative model, we applied binary dummy variable encoding. The **`Airport`** store classification was intentionally excluded from the active column set to serve as our absolute **reference baseline category**. 

### Coefficient Breakdown & Business Definitions:
* **Intercept (163,378.75):** The theoretical monthly baseline sales for an Airport location that has zero marketing spend, zero customer foot traffic, and zero inventory on hand.
* **`marketing_spend` (1.17):** Holding all other parameters constant, every dollar spent on marketing directly yields an additional **$1.17** in monthly sales. This confirms that marketing operates as a strong profit center.
* **`footfall` (33.60):** Controlling for alternate assets, each extra visitor generates an expected revenue increase of **$33.60**.
* **`inventory_availability_pct` (2,876.51):** For every 1% improvement in stock fulfillment rates, store revenue jumps by **$2,876.51**. This emphasizes how costly empty shelves are to the business.
* **`store_type_Mall` (-11,351.01):** Mall locations generate **$11,351.01 less** in monthly sales compared to an equivalent Airport location, all else being equal.
* **`store_type_High_Street` (-22,750.66):** High Street locations underperform Airport properties by an average of **$22,750.66** per month. However, with a high p-value of **0.01**, this variable is statistically weak and means High Street performance isn't reliably different from the Airport baseline.
* **`store_type_Residential` (-37,246.11):** Residential layouts show a major structural deficit, generating **$37,246.11 less** in monthly revenue than matching Airport hubs (P < 0.001).

### Selection Justification
Model 3 was chosen as our final analytical tool. It expands our explanatory power (R^2) to **81.47%**, successfully mitigates omitted variable bias, and accurately isolates the individual impact of each operational driver.