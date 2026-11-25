# Dynamic Pricing Design Projects

A portfolio of independent projects on price optimisation for online retail: estimating price elasticity from transaction data, turning it into a profit-maximising price, and (where the data allows) testing a price change.

Each project is its own GitHub repository with a reproducible pipeline, offline tests, an executed notebook with figures, and a README that states its data, method, and limitations.

## Projects

| # | Name | Dataset | Main method | Repository |
|---|------|---------|-------------|-------------|
| 1 | Price Elasticity from Retail Transactions | Online Retail (UK gift retailer, 2010–2011) | Within-product log-log regression with week fixed effects and HC3 errors | [dynamic-pricing-elasticity](https://github.com/Patotricks15/dynamic-pricing-elasticity) |
| 2 | Optimal Price Under Constant Elasticity | Online Retail, elasticities from project 1 | Closed-form profit maximum, clipped to the observed price band, with cost sensitivity | [dynamic-pricing-optimal-price](https://github.com/Patotricks15/dynamic-pricing-optimal-price) |
| 3 | Price A/B Readout (CUPED) | None yet: no candidate dataset has randomised price arms | Difference in means with CUPED adjustment and guardrails | [dynamic-pricing-ab-readout](https://github.com/Patotricks15/dynamic-pricing-ab-readout) |

## Blocked

- **Price A/B Readout (CUPED)** (project 3): the code and tests exist, but the readout has not been applied to any real test. None of the candidate datasets has a randomised price test with arm assignment, so it needs real experiment logs.

## Key limitations

- Project 1 estimates an **associative** elasticity. Prices and demand move together through promotions and seasonality, so it is not a causal price effect.
- Project 2 assumes a unit cost (60% of median price), because the data has no cost column. Its uplift is very sensitive to that assumption.
- The Online Retail dataset is licensed "other" on Kaggle, and its declared origin is a UK online gift retailer. Only code, notebooks, and figures are published; the raw data is not.

## Scope

This is part of a multi-plan portfolio. Projects are added here as they are completed; each repository listed above is self-contained and can be cloned, tested, and run independently.
