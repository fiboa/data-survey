# Berlin / Brandenburg, Germany

## Submission Details

- **Submitter (Affiliation):** Matthias Mohr
- **Data Provider (Legal Entity):** Land Brandenburg (Government)
- **Homepage:** https://geobroker.geobasis-bb.de/gbss.php?MODE=GetProductInformation&PRODUCTID=9e95f21f-4ecf-4682-9a44-e5f7609f6fa0

## Overview

The Digital Field Block Cadastre (DFBK) is an agricultural land cadastre. It contains all agriculturally used and eligible areas in the states of Brandenburg and Berlin with their location, size and other information. The DFBK serves as a reference system for checking area-related agricultural subsidy applications and consists of field blocks and landscape elements. A field block (FB) can be used by one or more farms and represents a contiguous agricultural area surrounded by permanent boundaries with predominantly uniform main land use. Landscape elements (LE) are landscape features such as hedges, rows of trees, copses and cairns that are located in or near the field block.
If a field block contains areas that cannot be used for agricultural purposes and are not an eligible landscape feature, these are marked as non-eligible areas (NBF).
The field blocks, landscape elements and NBF areas are digitized on the basis of aerial photographs (digital orthophotos) in the agricultural offices of the districts and independent cities as part of the EU IACS procedure (Integrated Administration and Control System). The data provided here in the form of FB and LE also contain numerical information on the proportion of land in areas relevant for funding (e.g. nature conservation areas, NATURA2000 areas and others).

## Data & Metadata

- **URL:** https://data.geobasis-bb.de/geofachdaten/Landwirtschaft/dfbk.zip
- **Documentation:**
  - https://geoportal.brandenburg.de/detailansichtdienst/render?view=gdibb&url=https://geoportal.brandenburg.de/gs-json/xml?fileid=9e95f21f-4ecf-4682-9a44-e5f7609f6fa0
  - https://www.geoportal-kommune-demo.de/docs/dfbk/Doku_DFBK.pdf
- **File Format:** Shapefile
- **Geometry Format (if different from data):** -
- **Metadata Format (if different from data):** -
- **Projection:** EPSG:25833 (UTM 33N)
- **License:** [Data licence Germany – attribution – Version 2.0](https://www.govdata.de/dl-de/by-2-0) / Proprietary

Data can also retrieved through their shop in other projections and file formats.

There are three different files included:

- NBF (Areas not eligible for state aid)
- LE (landscape elements)
- **FB (field blocks) - These are the actual field boundaries.**

### Properties

| Property   | Data Type | Constraints                                   | Description                                                  |
| ---------- | --------- | --------------------------------------------- | ------------------------------------------------------------ |
| FGUE_JAHR  | string    | 4 chars                                       | Year which the field is valid for                            |
| FB_ID      | string    | 16 chars                                      | Field block identifier (FLIK)                                |
| HBN_KAT    | string    | 34A, 34G, AL, AL-AF, DK, GL_ELP,GL, GL-MO, HE | Category of main land use (see below)                        |
| FL_BRUTTO  | number    | > 0                                           | Gross area in ha                                             |
| FL_NETTO_H | number    | > 0                                           | Net area in ha ("exkl. zugeordnetem Landschaftselement")     |
| KREIS_NR   | integer   | 5 digits                                      | Identifier for the regional office for agriculture           |
| TK10_BLATT | string    | 6 chars                                       | Paper of the 1:10,000 topographic map in which the center of where the center of gravity of the field block lies. Example: `4044SO` |
| GUELTVON_F | string    | ISO date                                      | Valid since                                                  |
| GUELTBIS_F | string    | ISO date                                      | Valid until                                                  |
| SHAPE_AREA | number    | > 0                                           | Area of the shape in m²                                      |
| SHAPE_LEN  | number    | > 0                                           | Length of the shape (i.e. boundary) in meters                |

The following values are valid for HBN_KAT:

- 34A = non-agricultural area on former arable land, eligible under Art. 32 (2b (i)) of Regulation 1307/2013
- 34G = non-agricultural area on former grassland, eligible under Art. 32 (2b (i)) of Regulation 1307/2013
- AL = arable land 
- AL-AF = Agroforestry on arable land
- DK = Permanent crops
- GL-ELP = Grassland management under "established local practices"
- GL = Grassland 40545 307026.8188
- GL-MO = Grassland created from arable land on moorland
- HE = Heath, no agricultural land

### Example

| Property   | Example Value    |
| ---------- | ---------------- |
| FGUE_JAHR  | 2024             |
| FB_ID      | DEBBLI0269205035 |
| HBN_KAT    | AL               |
| FL_BRUTTO  | 1.1354           |
| FL_NETTO_H | 1.1354           |
| KREIS_NR   | 69               |
| TK10_BLATT | 3543SO           |
| GUELTVON_F | 2024-01-01       |
| GUELTBIS_F | 2024-12-31       |

## API

| Standard | URL | Documentation |
| -------- | --- | ------------- |
| OGC WFS  | https://isk.geobasis-bb.de/ows/geobroker_l_dfbk_wfs?service=WFS&request=GetCapabilities | - |

