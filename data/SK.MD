# Slovakia

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** National Open Data Catalog (Národného katalógu otvorených dát)
- **Homepage:** https://data.slovensko.sk/

## Overview

Slovakia shares Field Blocks; Systém identifikácie poľnohospodárskych pozemkov (LPIS) and Crop fields (Hranice užívania)

LPIS is an agricultural land identification system. It represents the vector boundaries of agricultural land
and carries information about the unique code, acreage, culture/land use, etc., which is used as a reference
for farmers' applications, for administrative and cross-checks, on-site checks and also checks using remote
sensing methods.

## Data & Metadata

- **URL:** https://data.slovensko.sk/datasety/cc261225-7153-44a3-8ebf-05af207515c9
- **File Format:** Shapefile-zip
- **Projection:** EPSG:5514
- **License:** Open data

Download either:
    
- [Systém identifikácie poľnohospodárskych pozemkov (LPIS)](https://data.slovensko.sk/datasety/4c408849-80e9-41a2-8c93-08a65b7ce4fb) (field blocks) or 
- [Hranice užívania](https://data.slovensko.sk/datasety/cc261225-7153-44a3-8ebf-05af207515c9) (Crop fields)

### Properties

| Property   | **Data Type** | Constraints | Description     |
|------------|---------------|-------------|-----------------|
| ZKODKD     | String        |             | Identifier      |
| KODKD      | String        |             | code KD         |
| PARCELA    | String        |             | code KD         |
| PCUV       | Integer64     |             | code KD         |
| VYMERA     | Real          |             | Area            |
| Shape_Leng | Real          |             | Perimeter       |
| Shape_Area | Real          |             | Real Area       |
| LOKALITA_N | String        |             | Municipality    |
| KULTURA_SK | String        |             | Crop Group Code |
| KULTURA_NA | String        |             | Crop Group      |
| PLODINA    | String        |             | Crop Name       | 
| SUBJEKT_NA | String        |             | Applicant       |

