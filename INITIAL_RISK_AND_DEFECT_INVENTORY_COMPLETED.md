# Initial Risk and Defect Inventory

These are **suspected risks for later investigation**, not proven defects.

| ID | Worksheet / Area | Observation | Why It May Be a Problem | Evidence Available Now | Priority |
|---|---|---|---|---|---|
| R-01 | Cloud_Upgrade / Monthly_Model | Infrastructure stage changes when projected customer count reaches fixed thresholds. | Customer count may not represent actual technical load, concurrency, checks per hour, CPU, memory, uptime, or redundancy needs. | The formulas select Local Server, Cloud Stage 1, or Cloud Stage 2 using customer-count thresholds from Assumptions. | High |
| R-02 | Assumptions / Monthly_Model | Cost per lead, conversion rate, churn, and organic growth are fixed assumptions across the entire forecast. | Small changes in these values can materially change customer and revenue projections, so the model may look more certain than the evidence supports. | The same fixed inputs are reused in every monthly forecast row. | High |
| R-03 | Assumptions / Monthly_Model | Manager add-on revenue uses one average manager count for every customer. | Real customers may have different numbers of managers, which could make revenue estimates too high or too low. | Add-on revenue is calculated from one average-managers assumption and one included-manager assumption. | Medium |
| R-04 | Assumptions | Editable assumptions do not currently have strong range validation. | Negative ad spend, impossible percentages, zero cost per lead, or unrealistic manager counts could create invalid or misleading results. | Input cells are editable and clearly marked, but the workbook relies mainly on the user entering reasonable values. | High |
| R-05 | Monthly_Model | Some growth calculations produce fractional customers. | Fractions are mathematically useful for forecasting but may confuse users if they are interpreted as literal customer counts. | Paid and organic customer growth are continuous forecast values rather than rounded transactions. | Medium |
| R-06 | Actuals_Tracker | Actuals are entered manually. | Manual entry can create stale data, inconsistent definitions, and copy/paste errors. | The classroom tracker has manual input cells and no automated import process. | Medium |

## Initial Audit Summary
The most important areas to investigate are input validation, the sensitivity of the growth assumptions, and whether infrastructure decisions should be based on measured technical usage instead of customer count. None of these items is being presented as a proven defect in Assignment 3.2.
