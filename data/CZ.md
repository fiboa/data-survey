# Czech Crop fields

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Czech Ministry of Agriculture (Ministr Zemědělství)
- **Homepage:** https://mze.gov.cz/public/portal/mze/farmar/LPIS

## Overview

Czech offers open data sets for fields as part of the implementation of the Inspire directive.

Here we take not of the Field Blocks "Díly půdních bloků" (DPB) and Crop Fields "Plodiny".

## Data

- **URL:** https://mze.gov.cz/public/portal/mze/farmar/LPIS/export-lpis-rocni-shp
- **Documentation:** https://mze.gov.cz/public/app/lpisext/lpis/ng/plodiny-plpis/ (Crop index)
- **File Format:** Shapefile/zip
- **Projection:** EPSG:5514 or EPSG:4258
- **License:** CC-0 (Publicly distributed as part of the Inspire directive)

### Properties

Crop Fields (Plodiny)

| Property   | Data Type  | Constraints | Description |
|------------|------------|-------------|-------------|
| ID_UZ      | Integer64  |             |             |
| JI         | Integer64  |             |             |
| ID_SZR     | Integer64  |             |             |
| ICO        | String     |             |             |
| DPB_ID     | Integer64  |             |             |
| DPB_CTVERE | String     |             |             |
| DPB_ZKOD   | String     |             |             |
| DPB_VYMERA | Real       |             |             |
| ROK        | Integer    |             |             |
| EKO        | String     |             |             |
| KULTURAKOD | String     |             |             |
| ZAKRES_ID  | Integer64  |             |             |
| OP_ID      | Integer64  |             |             |
| OP_KOD     | String     |             |             |
| TIT_ID     | Integer64  |             |             |
| TIT_KOD    | String     |             |             |
| PLODINA_ID | String     |             | Crop code   |
| PLOD_NAZE  | String     |             | Crop name   |
| DEKL_VYM   | Real       |             |             |
| ZAKRES_VYM | Real       |             |             |
| DATUM_REP  | String     |             | Date        |
| REGCISZAD  | String     |             |             |
| CISPREDTIS | String     |             |             |
| CISJED     | String     |             |             |
| DOPLNKOVY  | String     |             |             |
| DATUM_VYS  | String     |             |             |
| OBEC_NAZEV | String     |             |             |
| OBEC_KOD   | Integer    |             |             |
| OKRES_NAZE | String     |             |             |
| OKRES_KOD  | Integer    |             |             |

## API

https://mze.gov.cz/public/portal/mze/farmar/LPIS/ws-lpis
