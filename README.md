####  ISDA SIMM v2.7 Parameters updated for this calculation by Abukar Ali. Date: 2025-06-23

To calcute an initial margin required from a given counterparty for uncleared derivative trades
that qualify to post Iniitial margin using the ISDA Method.  we will require the following: 

- standard input file that contains sensitify data such as delta, gamma, vega for all traded derivative positions
- from the bank's Front office system. such data are aggregated into CRIF file which used an input file for SIMM calculation.
- Next, we will need to read the latest or most recent risk weights and parameters defined by ISDA for SIMM calculations. 
- in this repository, we have a file called v2_7.py - a python input file that has contains all the ISDA Defined risk weights, correlation input data, etc  
- this would take a long time to manually input these data, we have used the 2023 file which contained numbering for the relant section of the data from the ISDA PDF
- i have then used the older file as a guide and asked Deepseek to populate the file using the 2024 updated data - the result was amazing. 

**** DeepSeek Helped Reduce manual input time to only 5 minutes. 

*** (but initially, sometime is required for prompting and QA checks)

- ChatGPT was full of errors and didnt even follow the format of the required file, but with the correct prompt, Deepseek was spot on and 
- as required, it only too few minutes.  Obviously, We dont rely on this fully, so we made sure, we read the pdf line by line and cross check to ensure, all is 100% correct.  
  
  
      INCORRECT or any MIsspecication can lead to impact on your SIMM calculaton - 
      there is always a risk that something is mistyped which can happen both via deepseek or by manual entry.  

 - the resposity we have all the files we need:  

  - aggregate margins.py files
  - aggregate sensitivies.py files
  - margin risk.py files
  - source folder:  contains wnc.py:  this is the file you need to specify that you are using the v2_7.py file. 

 - ok so, once we have the inputs- both the CRIF and v2_7.py, and all the above files 

- we use the main file to run our final SIMM Calculations. Table below shows an output of the SIMM calculations. 

- NOTE, since we do not have actuall sensitivy data, we have created a synthetic data to allow the calculation. but you can easilly update CRIF file for the real thing :-)

The parameters below can be found at https://www.isda.org/a/2IOgE/ISDA_SIMM_v2.7_PUBLIC.pdf

ISDA SIMM v2.7 Parameters updated. Date: 2024-12-07



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