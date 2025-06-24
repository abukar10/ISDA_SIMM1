### ISDA SIMM v2.7 Parameters updated for this calculation by Abukar Ali. Date: 2025-06-23
### The parameters below can be found at https://www.isda.org/a/2IOgE/ISDA_SIMM_v2.7_PUBLIC.pdf

### ISDA SIMM v2.7 Parameters updated. Date: 2024-12-07



## Getting Started
  - the ISDA defined input data is saved under the file v2_7 under weights_and_corr folder. 

  - Run python -m main

## Results Example

| SIMM Total         | Add-On         | Product Class | SIMM_ProductClass | Risk Class      | SIMM_RiskClass    | Risk Measure      | Value             |
|--------------------|----------------|---------------|-------------------|-----------------|-------------------|-------------------|-------------------|
| 17,160,305,964.99  | 865,685,368.85 | Commodity     | 339,045,085.73    | Commodity       | 339,045,085.73    | Curvature         | 40,704,987.4      |
|                    |                |               |                   |                 |                   | Delta             | 189,379,973.36    |
|                    |                |               |                   |                 |                   | Vega              | 108,960,124.97    |
|                    |                | Credit        | 14,753,961,065.17 | CreditNonQ      | 12,403,098,591.87 | Curvature         | 37,279.59         |
|                    |                |               |                   |                 |                   | Delta             | 12,401,687,156.64 |
|                    |                |               |                   |                 |                   | Vega              | 1,374,155.64     |
|                    |                |               |                   | CreditQ         | 3,646,291,459.95  | BaseCorr          | 8,222,230.0       |
|                    |                |               |                   |                 |                   | Curvature         | 33,337.56         |
|                    |                |               |                   |                 |                   | Delta             | 3,635,615,442.41  |
|                    |                |               |                   |                 |                   | Vega              | 2,420,449.99     |
|                    |                |               |                   | Equity          | 82,199,370.35     | Curvature         | 0.0               |
|                    |                |               |                   |                 |                   | Delta             | 82,199,370.35     |
|                    |                |               |                   |                 |                   | Vega              | 0.0               |
|                    |                |               |                   | FX              | 7,185,584.22      | Curvature         | 0.0               |
|                    |                |               |                   |                 |                   | Delta             | 7,185,584.22      |
|                    |                |               |                   |                 |                   | Vega              | 0.0               |
|                    |                |               |                   | Rates           | 196,024,739.4     | Curvature         | 0.0               |
|                    |                |               |                   |                 |                   | Delta             | 196,024,739.4     |
|                    |                |               |                   |                 |                   | Vega              | 0.0               |
|                    |                | Equity        | 459,818,122.84    | Equity          | 310,604,063.19    | Curvature         | 13,823,144.02     |
|                    |                |               |                   |                 |                   | Delta             | 199,875,534.81    |
|                    |                |               |                   |                 |                   | Vega              | 96,905,384.36     |
|                    |                |               |                   | Rates           | 318,008,431.48    | Curvature         | 0.0               |
|                    |                |               |                   |                 |                   | Delta             | 318,008,431.48    |
|                    |                |               |                   |                 |                   | Vega              | 0.0               |
|                    |                | RatesFX       | 741,796,322.4     | FX              | 26,212,645.82     | Curvature         | 9,185,361.42      |
|                    |                |               |                   |                 |                   | Delta             | 12,089,717.24     |
|                    |                |               |                   |                 |                   | Vega              | 4,937,567.16      |
|                    |                |               |                   | Rates           | 737,672,355.96    | Curvature         | 1,706.73          |
|                    |                |               |                   |                 |                   | Delta             | 737,650,204.98    |
|                    |                |               |                   |                 |                   | Vega              | 20,444.24         |

## Warning
If you intend to implement this for any commercial purpose, reach out to ISDA SIMM™ (isdalegal@isda.org)