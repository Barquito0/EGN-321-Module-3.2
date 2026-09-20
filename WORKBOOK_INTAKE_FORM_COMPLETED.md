# Workbook Intake Form

## Student
- Name: Marco Ruiz
- Course / Section: EGN 321 - Module 3
- Date: September 20, 2026

## Workbook
- Original workbook name: No pre-existing operational workbook; a synthetic classroom equivalent was created from SyntraTech's real planning needs.
- Sanitized submission name: `SyntraTech_Capstone_Candidate_SANITIZED_SYNTHETIC.xlsx`
- File type: `.xlsx`
- Approximate number of worksheets: 7
- Approximate number of formula cells: about 160+
- Macros present? No
- External links present? No
- Protected sheets/workbook? No

## Source
- Where did the workbook come from?  
  It was created from a real planning problem at SyntraTech. SyntraTech needs to plan pricing, customer growth, advertising spending, operating costs, and future infrastructure upgrades. The classroom workbook uses synthetic values instead of private business data.

- What type of organization/process uses it?  
  Early-stage software / automation business planning.

- Do you have permission to use a sanitized copy for class? Yes. The student created and owns the synthetic classroom artifact.

- Who is the primary user?  
  Founder / business owner. A future operations or finance manager could also use the model.

## Purpose
- What business/engineering process does it support?  
  Pricing, customer-acquisition planning, operating-cost forecasting, infrastructure planning, and basic financial forecasting.

- What question does the workbook answer?  
  How could different pricing, advertising, customer-growth, support-cost, and infrastructure assumptions affect SyntraTech's customers, revenue, net income, cash, and cloud-upgrade timing?

- What decision depends on the result?  
  Subscription pricing, additional-manager pricing, advertising budget, support planning, and when to consider moving from the local server to larger cloud infrastructure.

- How often is it used?  
  Intended for monthly planning and for scenario reviews whenever pricing, marketing, or infrastructure assumptions change.

## Inputs

| Input | Meaning | Unit | Source |
|---|---|---|---|
| Current paying customers | Starting customer base | customers | Synthetic classroom baseline |
| Base subscription price | Monthly price per customer | $/customer/month | Synthetic planning assumption |
| Additional manager fee | Add-on fee above included managers | $/manager/month | Synthetic planning assumption |
| Advertising spend | Planned monthly marketing budget | $/month | Synthetic planning assumption |
| Cost per qualified lead | Estimated acquisition cost before conversion | $/lead | Synthetic planning assumption |
| Lead-to-customer conversion | Share of qualified leads that become customers | % | Synthetic planning assumption |
| Annual churn rate | Expected customer loss rate | %/year | Synthetic planning assumption |
| Average managers per DSP | Expected manager seats per customer | managers/customer | Synthetic planning assumption |
| Support hours | Expected support effort | hours/customer/month | Synthetic planning assumption |
| Cloud thresholds/costs | Future infrastructure assumptions | customers and $ | Synthetic planning assumption |

## Outputs

| Output | Meaning | Unit | Who Uses It |
|---|---|---|---|
| Ending customers | Projected customer base by month | customers | Founder / operations |
| Total revenue | Projected monthly and annual revenue | $ | Founder / finance |
| Net income | Revenue minus modeled operating costs | $ | Founder / finance |
| Ending cash | Simplified projected cash position | $ | Founder |
| Pricing scenario contribution | Estimated recurring contribution by plan | $/month | Founder / sales planning |
| Infrastructure stage | Local Server, Cloud Stage 1, or Cloud Stage 2 | stage | Founder / technical operations |
| Revenue variance | Actual revenue minus forecast | $ | Founder / finance |

## Initial Concerns
- What appears difficult to understand?  
  Several business assumptions feed chained formulas across multiple sheets. The relationship between growth, pricing, advertising, support, and infrastructure is easier to follow than a single large formula, but it still requires documentation.

- What appears fragile?  
  Cloud-upgrade thresholds rely on customer count instead of measured system load. Forecast results also depend heavily on fixed marketing and churn assumptions.

- What may be wrong?  
  I suspect that customer-count thresholds, average manager counts, and fixed acquisition assumptions may not represent real operating conditions as SyntraTech grows. These are not proven defects yet.

- What would you like to improve?  
  Input validation, scenario testing, measured infrastructure triggers, actual-versus-forecast automation, testing, documentation, and a clearer Python interface.
