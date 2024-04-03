# Lower Saxony, Germany

## Submission Details

- **Submitter (Affiliation):** Matthias Mohr
- **Data Provider (Legal Entity):** ML/SLA Niedersachsen (Government)
- **Homepage:** https://sla.niedersachsen.de/landentwicklung/LEA/

## Overview

Field blocks in Lower Saxony in Germany.

## Data & Metadata

- **URL:** https://sla.niedersachsen.de/mapbender_sla/download/FB_NDS.zip
- **Documentation:** ?
- **File Format:** Shapefile
- **Geometry Format (if different from data):** -
- **Metadata Format (if different from data):** ?
- **Projection:** EPSG:25832 (UTM 32N)
- **License:** [Data licence Germany – attribution – Version 2.0](https://www.govdata.de/dl-de/by-2-0)

### Properties

| Property   | Data Type | Constraints     | Description                                                  |
| ---------- | --------- | --------------- | ------------------------------------------------------------ |
| FLIK       | string    | 16 chars        | Area identifier for field blocks. Example: `DENIHB0412500015` |
| FLAECHE    | number    | > 0             | Area in ha                                                   |
| ANT_JAHR   | string    | Year | Year of claim, e.g. `2024` |
| BNK        | string    | AFF\*, AL, AL\*, DK, DK\*, GL, GL\*, MB, SO, SO* | Category of land use, short code. |
| BNK_TXT | string    | see below | Textual representation of BNK in German |
| STAND | string | Date | Last update (e.g. `2024-01-31`) |
| SHAPE_Leng | number    | > 0                                              | Length of boundary in m                                      |
| SHAPE_Area | number    | > 0                                              | Area in m²                                                   |

Mapping between BNK and BNK_TXT:

- AFF\* = Aufforstungsfläche
- AL = Ackerland
- AL\* = Ackerland
- DK = Dauerkulturen
- DK\* = Dauerkulturen
- GL = Grünland
- GL\* = Grünland
- MB = Mischblock
- SO = Sonstiges
- SO* = SO nicht beihilfefähig

## API

| Standard | URL | Documentation |
| -------- | --- | ------------- |
| OGC WFS | https://sla.niedersachsen.de/agrarfoerderung/agrar_ref/wfs?service=WFS&version=2.0.0&request=GetFeature&typeName=agrar_ref:feldbloecke&count=50&outputFormat=application%2Fgml%2Bxml%3B%20version%3D3.2& | - |

