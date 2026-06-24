# parthbudhia_bitsom_ba_2511121_part3_regression_insights

# Part 3: Regression-Based Business Insights & Model Interpretation

## Business Problem Summary
The executive leadership team of our retail chain wants to understand what structural operational factors drive monthly sales performance across its store footprint. This project leverages ordinary least squares (OLS) linear regression modeling to isolate the impacts of marketing budgets, floor traffic volumes, stock fulfillment rates, and brick-and-mortar store formats. The final insights provide a data-driven blueprint for maximizing capital allocation efficiency and operational returns.

## Dataset Profile & Data Variables
* **Dependent Variable ($Y$):** `monthly_sales` (Continuous numerical revenue value).
* **Numerical Independent Variables ($X$):** `marketing_spend`, `footfall`, `avg_discount_pct`, `staff_count`, `inventory_availability_pct`, `competitor_distance_km`, `holiday_flag`, `customer_rating`.
* **Categorical Variables:** `store_type` (`Mall`, `High Street`, `Residential`, `Airport`), `region` (`East`, `West`, `North`, `South`).
* **Variables Requiring Transformation:** `store_type` was converted into binary dummy variables to be processed in a linear model framework.
* **Variables Excluded/Not Useful:**
  * `store_id`: A unique alphanumeric text identifier with no mathematical value.
  * `month`: Parsed as a historical date code, not helpful for cross-sectional regression.
  * `monthly_profit`: A downstream financial metric highly collinear with sales, which would cause data leakage if used as a predictor.

## Regression Approach & Dummy Variable Mapping
We adopted an iterative regression building pipeline, starting from single-predictor baselines to capture isolated factors before constructing an integrated multiple linear regression system. Categorical store formats were handled using binary dummification. To avoid the mathematical redundancy known as the Dummy Variable Trap, **`Airport`** was chosen as the reference baseline category.

## Model Summary & Selection
* **Simple Model 1 (Marketing Focus):** $R^2 = 0.1574$ — Marketing explains $15.74\%$ of monthly store sales variance.
* **Simple Model 2 (Footfall Focus):** $R^2 = 0.7348$ — Foot traffic explains $73.48\%$ of monthly store sales variance.
* **Multiple Regression Model (Integrated Framework):** $R^2 = 0.8147$ — Explains **81.47%** of total variance by combining operational variables alongside store types. This was chosen as our final analytical tool due to its high explanatory value and balanced errors.

## Key Executive Recommendation
1. **Optimize Supply Chains:** Product stock depth has incredible marginal leverage ($2,876.51). Maximizing inventory availability is the fastest route to capturing latent market revenue.
2. **Pivot Capital Away from Residential Formats:** Residential store configurations structurally generate **$37,246.11 less** in monthly revenue compared to Airport hubs under identical operational asset levels.
3. **Sustain Core Marketing Budgets:** Marketing spend is a verified profit center, yielding a positive marginal cash pipeline return ($1.17).

## Required Repository Artifact Checklist
* `screenshots/simple_regression_output1.png`
* `screenshots/simple_regression_output2.png`
* `screenshots/multiple_regression_output.png`
* `screenshots/residuals_preview.png`
* `screenshots/model_comparison_preview.png`

---

## Assumptions and Limitations
* **Linearity Assumption:** Assumes consumer response paths scale linearly without steep diminishing returns.
* **Omitted Feature Variables:** The modeling matrices do not capture macro inflation spikes, localized pricing promotions, or shifts in regional manager experience levels.
