# Model Evaluation & Cross-Comparison Analysis

A formal technical and business evaluation was performed to contrast our simple single-predictor baselines against the comprehensive multiple regression model.

| Evaluation Metric | Model 1: Simple Marketing Model | Model 2: Simple Footfall Model | Model 3: Comprehensive Multiple Regression |
| :--- | :--- | :--- | :--- |
| **Model Name** | Baseline Marketing Predictor | Baseline Visitor Volume Predictor | Integrated Operational & Format Framework |
| **Variables Used** | **Dependent:** `monthly_sales`<br>**Independent:** `marketing_spend` | **Dependent:** `monthly_sales`<br>**Independent:** `footfall` | **Dependent:** `monthly_sales`<br>**Independent:** `marketing_spend`, `footfall`, `inventory_availability_pct`, `store_type_Mall`, `store_type_High_Street`, `store_type_Residential` |
| **R-squared** | **0.1574** (Explains 15.74% of sales variance) | **0.7348** (Explains 73.48% of sales variance) | **0.8147** (Explains 81.47% of sales variance) |
| **Significant Variables** | `marketing_spend` <br>(P < 0.001) | `footfall` <br>(P < 0.001) | `marketing_spend`, `footfall`, `inventory_availability_pct`, `store_type_Mall`, `store_type_Residential` <br>(All P < 0.05) |
| **Business Usefulness** | **Low.** Over-emphasizes promotional spend while ignoring real-world physical limitations like store footprint capacities and traffic constraints. | **Moderate.** Clearly shows that physical visitor density is a major factor for top-line revenue, but doesn't provide tactical operational levers. | **High.** Provides a robust, highly predictive framework that allows the leadership team to simultaneously optimize marketing budgets, inventory levels, and geographic store selections. |
| **Limitations** | Suffers from severe omitted variable bias, making its single coefficient too unstable to support independent capital deployment choices. | Footfall is an intermediate outcome; the model does not explain *why* footfall changes or how internal store parameters drive it. | Does not model interactive terms (such as the combined effect of high discounts alongside holiday spikes) or localized competitive pressures. |