# Portugal Crop Fields

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** IPAP - Instituto de Financiamento da Agricultura e Pescas
- **Homepage:** https://www.ifap.pt/isip/ows/

## Overview

Field blocks and Crop Fields identified in the Parcel Identification system (iSIP) as applied-for in the CAP.
Updated annually (https://www.ifap.pt/sip-informacao-basica), organized by NUTII until 2018. 

Three different data sets are published, we wil use the Crop Fields.

- Field Blocks (Parcelas)
- Land Cover (Ocupações de solo)
- Crop Fields (Culturas)

## Data

- **URL:** https://www.ifap.pt/isip/ows/resources/2023/Continente.gpkg
- **Documentation:** https://www.ifap.pt/isip/ows/resources/desc_informacao.pdf (Portugese)
- **Crop codes:** https://www.ifap.pt/isip/ows/resources/Culturas.zip
- **File Format:** GeoPackage
- **Projection:** EPSG:3763
- **Contact:** dadosgeograficos@ifap.pt
- **License:** "no conditions apply". Seems to refer to Inspire license https://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/noConditionsApply

### Properties

| Property     | Data Type   | Constraints | Description                   |
|--------------|-------------|-------------|-------------------------------|
| OBJECTID     | int64       |             |                               |
| CUL_ID       | int         |             | Field block identifier        |
| CUL_CODIGO   | string      | 3 chars     | Code for crop                 |
| OSA_ID       | Integer int |             | Crop field identifier         |
| CT_português | string      | 255 chars   | Crop name (Portugese)         |
| Shape_Length | Real (0.0)  |             | Perimeter length in meters    |
| Shape_Area   | Real (0.0)  |             | Surface area in square meters |

### Example

See https://www.ifap.pt/isip/ows/resources/parcelas.pdf

## API

| Standard | URL                                                                            |
|----------|--------------------------------------------------------------------------------| 
| OGC WMS  | https://www.ifap.pt/isip/ows/isip.data/wms?service=wms&request=getcapabilities |
| OGC WFS  | https://www.ifap.pt/isip/ows/isip.data/wfs?service=wfs&request=getcapabilities |
