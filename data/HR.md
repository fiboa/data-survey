# Croatia Crop fields (ARKOD Plots)

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Agencija za plaćanja u poljoprivredi, ribarstvu i ruralnom razvoju objavila
- **Homepage:** https://www.apprrr.hr/prostorni-podaci-servisi/

## Overview

ARKOD is a record of the use of agricultural land in the territory of the Republic of Croatia,
which is maintained in digital graphic form by the Agency for Payments. ARKOD parcels represent uninterrupted
areas of agricultural land cultivated by one farmer, classified according to the type of use of agricultural land. 

Registration of agricultural land - vectorization of ARKOD polygons is carried out by the method of
photointerpretation of agricultural land on DOF bases in a scale of 1:5000 in branches of the Agency for Payments,
statements of farmers on the use of agricultural land with proof of ownership or possession.
ARKOD data is used within the IAKS system for monitoring subsidies related to surfaces,
which is technically carried out by annually filling out the Single Request through the AGRONET application.
Changes to the ARKOD data are carried out: at the request of the farmer, who is obliged to report the changes
within 30 days of their occurrence, at the request of the landowner (disagreeing and uninformed),
during the renewal of the DOF (annual dynamics of 50% of the state's territory),
based on the results of the administrative controls, field controls, rapid field checks,
agricultural inspection solutions, by implementing visual checks, ARKOD quality control results and
administrative decisions of the Agency for Payments in Agriculture, Fisheries and Rural Development.

## Data

- **URL:** https://www.apprrr.hr/prostorni-podaci-servisi/
- **File Format:** GeoPackage
- **Projection:** EPSG:9122
- **License:** Not stated . Data is downloadable.

### Properties

| Property                 | Data Type | Constraints | Description                   |
|--------------------------|-----------|-------------|-------------------------------|
| land_use_id              | Real      |             | Land cover code               |
| home_name                | String    |             |                               |
| area                     | Real      |             | area                          |
| perim                    | Real      |             | perimeter                     |
| slope                    | Real      |             | slope                         |
| z_avg                    | Real      |             | average height                |
| eligibility_coef         | Real      |             | eligibility_coefficient       |
| mines_status             | String    |             | mines status                  |
| mines_year_removed       | Integer   |             | Year of mine removal          |
| water_protect_zone       | String    |             | Water protection zone         |                 
| natura2000               | Real      |             | Area of natura2000 protection |
| natura2000_ok            | String    |             |                               |
| natura2000_pop           | Real      |             |                               |
| natura2000_povs          | Real      |             |                               |
| anc                      | Integer   |             |                               |
| anc_area                 | Real      |             |                               |
| rp                       | Integer   |             |                               |
| sanitary_protection_zone | String    |             |                               |                            
| tvpv                     | Integer   |             |                               |                             
| ot_nat                   | Integer   |             |                               |
| ot_nat_area              | Real      |             |                               |
| irrigation               | Integer   |             | has irrigation                |                             
| irrigation_source        | Integer   |             | 0                             |             
| irrigation_type          | Integer   |             | irrigation type               |                             
| jpaid                    | String    |             |                               |

## API (optional)

| Standard | URL                                                                     | Documentation |
|----------|-------------------------------------------------------------------------|---------------|
| OGC WFS  | https://servisi.apprrr.hr/NIPP/wfs?request=getCapabilities              | -             |
| OGC WMS  | https://servisi.apprrr.hr/NIPP/wms?service=WMS&request=GetCapabilities  | -             |
