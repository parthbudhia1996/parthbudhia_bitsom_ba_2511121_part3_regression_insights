# Residual Analysis & Operational Anomaly Diagnostics

Residual calculations were extracted directly from the predictions sheet using the standard formula:  
{Residual} = {Actual Sales} - {Predicted Sales}

### Top 5 Under-Predicted Store Periods (Largest Positive Residuals)
*The model predicted lower sales, but these specific periods significantly outperformed expectations.*
1. **Observation Row 279:** Actual Sales: `$813,316.71` | Predicted Sales: `$710,897.14` | **Residual: +$102,419.57**
2. **Observation Row 114:** Actual Sales: `$820,519.04` | Predicted Sales: `$718,718.92` | **Residual: +$101,800.12**
3. **Observation Row 108:** Actual Sales: `$713,611.16` | Predicted Sales: `$614,209.76` | **Residual: +$99,401.40**
4. **Observation Row 121:** Actual Sales: `$914,544.17` | Predicted Sales: `$815,549.18` | **Residual: +$98,994.99**
5. **Observation Row 192:** Actual Sales: `$735,786.64` | Predicted Sales: `$644,356.17` | **Residual: +$91,430.47**

* **Business Meanings:** These large positive exceptions point to highly successful localized factors not fully captured by national metrics. This includes events like viral social media exposure, temporary pop-up community festivals near the storefront, or an immediate competitor shutting down for remodeling.

### Top 5 Over-Predicted Store Periods (Largest Negative Residuals)
*The model projected high sales, but these store periods underperformed significantly.*
1. **Observation Row 66:** Actual Sales: `$685379.08` | Predicted Sales: `$841983.82` | **Residual: -$156604.75**
2. **Observation Row 87:** Actual Sales: `$627171.9` | Predicted Sales: `$749758.63` | **Residual: -$122586.74**
3. **Observation Row 44:** Actual Sales: `$595467.6` | Predicted Sales: `$715597.90` | **Residual: -$120130.30**
4. **Observation Row 33:** Actual Sales: `$641865.03` | Predicted Sales: `$746610.00` | **Residual: -$104744.97**
5. **Observation Row 26:** Actual Sales: `$800451.94` | Predicted Sales: `$902183.86` | **Residual: -$101731.92**

* **Business Meanings:** These negative anomalies trace back to localized operational disruptions. Examples include major road construction limiting parking lot access, extended in-store Point-of-Sale (POS) software outages, or a severe mismatch in local inventory mix that left popular core items out of stock despite high overall volume.

### Store Type Over/Under-Prediction Structural Bias
Analyzing our model errors reveals a clear structural trend: **Airport formats are regularly under-predicted** during high-velocity traffic months, proving these locations benefit from unique impulse buying patterns that standard linear baselines miss. Conversely, **Residential strip centers are systematically over-predicted**. This indicates that neighborhood traffic does not convert into large, high-value shopping baskets as easily as traffic in premium transit hubs.