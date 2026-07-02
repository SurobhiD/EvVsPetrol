# EV vs Petrol Car Cost of Ownership App

## Purpose

Build a decision-support application for Indian car buyers to compare the total cost of ownership of electric vehicles (EVs) and petrol cars. The app should help users understand which option is financially better for their driving pattern, location, purchase budget, and ownership period.

The application should not simply compare showroom prices. It should model the full ownership picture, including purchase price, financing, fuel or charging cost, maintenance, insurance, taxes, incentives, resale value, and usage assumptions.

## Target Users

- Individual car buyers in India deciding between an EV and a petrol car.
- Families comparing two specific car models before purchase.
- Fleet owners or high-mileage users estimating long-term savings.
- Auto researchers, reviewers, and advisors who need a transparent comparison tool.

## Core User Goal

Users should be able to answer:

> "For my usage and assumptions, should I buy the EV or the petrol car?"

The app should produce a clear recommendation and show the reasoning behind it.

## Key Capabilities

### 1. Model-to-Model Comparison

Users can enter or select:

- EV car model.
- Petrol car model.
- City or state in India.
- Expected ownership period.
- Monthly or annual driving distance.

The tool should compare both vehicles side by side.

### 2. Editable Assumptions

Users should be able to change assumptions and see the dashboard update automatically.

Important assumptions include:

- On-road price.
- Down payment.
- Loan amount, interest rate, and loan tenure.
- Annual kilometres driven.
- Petrol price per litre.
- Electricity price per kWh.
- Public charging share versus home charging share.
- EV efficiency in km/kWh.
- Petrol mileage in km/litre.
- Annual maintenance cost.
- Insurance cost.
- Battery replacement assumption, if applicable.
- Road tax and registration cost.
- Government incentives or subsidies.
- Expected resale value.
- Inflation or annual price escalation for petrol, electricity, insurance, and maintenance.

### 3. Automatic Data Lookup

Users should be able to provide car model names, and the app should attempt to fetch values from reliable internet sources.

The fetched data may include:

- Ex-showroom price.
- On-road price by city, where available.
- Claimed mileage or certified range.
- Battery capacity.
- Charging specifications.
- Petrol engine fuel efficiency.
- Insurance estimate.
- Road tax and registration rules.
- Current petrol price by city.
- Electricity tariff by state or distribution company.
- Available EV subsidies or incentives.
- Estimated resale value or depreciation benchmarks.

All automatically fetched values should be visible and editable. The app should show the source and retrieval date for each fetched value.

### 4. Decision Matrix

The app should calculate a decision score for each car using financial and practical factors.

Suggested decision dimensions:

- Total cost of ownership.
- Monthly cash flow impact.
- Fuel or charging savings.
- Break-even period.
- Resale value risk.
- Maintenance burden.
- Range or refuelling convenience.
- Charging availability.
- Environmental impact.
- Policy or subsidy advantage.

Users should be able to adjust the weight of each decision factor.

### 5. Dashboard

The dashboard should update whenever assumptions change.

It should show:

- Total cost of ownership for each car.
- Year-by-year ownership cost.
- Monthly EMI and running cost.
- Fuel versus charging cost.
- Maintenance and insurance cost.
- Break-even month or year.
- Savings over the ownership period.
- Sensitivity analysis for fuel price, electricity price, usage, and resale value.
- Final recommendation with explanation.

## Recommendation Logic

The app should recommend the better option based on:

- Lowest total cost of ownership.
- User-defined decision weights.
- Break-even period compared with planned ownership period.
- Risk flags, such as uncertain resale value, high public charging dependency, or unusually low annual usage.

The recommendation should be explainable. For example:

> "The EV is recommended because it saves Rs. 3.2 lakh over 6 years and breaks even in year 4. This assumes 1,200 km of monthly driving and 80% home charging."

If the comparison is close, the app should say so instead of forcing a false certainty.

## Data Principles

- Prefer official manufacturer pages, government sources, fuel price APIs, electricity tariff documents, and trusted automotive sites.
- Store the source URL, source name, and date fetched for every imported value.
- Treat internet data as a starting assumption, not as final truth.
- Allow users to override every fetched value.
- Mark stale data and prompt refresh when appropriate.
- Separate claimed mileage/range from real-world efficiency assumptions.

## India-Specific Requirements

The app should account for India-specific ownership factors:

- Ex-showroom versus on-road pricing.
- State-level road tax differences.
- City-level petrol price differences.
- State electricity tariff variation.
- Home charging and public fast-charging price differences.
- FAME or successor EV policy incentives, if active.
- State EV subsidies and registration benefits.
- Indian driving patterns and real-world mileage/range gaps.
- Resale market uncertainty for EVs.

## Suggested Screens

### Compare

Primary workspace where users choose two cars, enter location and usage, and view the side-by-side result.

### Assumptions

Detailed editable inputs for prices, financing, running costs, depreciation, incentives, and usage.

### Dashboard

Charts, summaries, break-even analysis, and final recommendation.

### Data Sources

Source list for all fetched values, including confidence level and last updated date.

### Scenarios

Saved scenarios such as:

- Low usage city driver.
- High usage commuter.
- Mostly public charging.
- Mostly home charging.
- Short ownership period.
- Long ownership period.

## Non-Goals

- The app should not guarantee exact future savings.
- The app should not provide financial, tax, or legal advice.
- The app should not hide assumptions behind a black-box recommendation.
- The app should not rely only on manufacturer-claimed figures without real-world adjustment.

## Success Criteria

- A user can compare one EV and one petrol car in less than five minutes.
- Every major cost assumption is visible and editable.
- The dashboard updates immediately after assumption changes.
- The recommendation is explainable and traceable to user inputs.
- Automatically fetched values include source attribution.
- The app works well for Indian cities, prices, policies, and ownership patterns.

## Future Enhancements

- Add diesel, hybrid, and CNG comparisons.
- Add emissions comparison based on grid electricity mix.
- Add charging station availability by route or city.
- Add multiple-car shortlist comparison.
- Add PDF or shareable report export.
- Add family budget and affordability checks.
- Add API integrations for live fuel prices, tariffs, and vehicle data.

