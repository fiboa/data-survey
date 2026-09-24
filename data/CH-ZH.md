# Zürich, Switzerland

## Submission Details

- **Submitter (Affiliation):** Saidy Barry, moreGeo GmbH
- **Data Provider (Legal Entity):** Kanton Zürich, Amt für Landschaft und Natur (Government)
- **Homepage:** https://www.zh.ch/de/umwelt-tiere/landwirtschaft.html

## Overview

The usage areas ("Landwirtschaftliche Kulturflächen") cultivated by Zürich farms, one WFS layer per year since
2017, compatible with the federal model 153.1. 2017 and 2018 do not cover all municipalities. The layers include
the fields of Zürich farms in neighbouring cantons (`outside_canton`, two per cent of the rows), as does the
canton's file on [geodienste.ch](CH.md).

## Data

- **URL:** https://maps.zh.ch/wfs/OGDZHWFS (WFS 2.0), layers `ms:ogd-0170_giszhpub_lw_nutzungsflaechen_<year>_f` for 2017 to 2025; a whole year in one request with `COUNT=200000&OUTPUTFORMAT=application/shapefile`
- **Documentation:** https://www.geolion.zh.ch/geodatensatz/show?gdsid=170
- **File Format:** WFS (Shapefile, GeoJSON, GML, CSV output)
- **Projection:** EPSG:2056 (CH1903+ / LV95)
- **License:** [opendata.swiss terms of use, Open use](https://opendata.swiss/terms-of-use#terms_open); [Kanton Zürich terms of use](https://geo.zh.ch/terms-of-use)
- **Attribution:** Kanton Zürich, Amt für Landschaft und Natur

Features per year: 11,777 (2017), 63,987 (2018), 101,690 (2019), 106,152 (2020), 127,717 (2021), 140,229 (2022),
143,016 (2023), 145,437 (2024), 146,335 (2025). `blw_nr` is the federal usage code, zero-padded; `blw_name` the
canton's abbreviated name; `flaeche` is in ares; `gis_nr` equals `nutzungsidentifikator` on geodienste.ch. Code
`0399` ("Nutzung bestimmen") marks usages not yet classified (224 rows in 2025). `farm_id` identifies the farm and
is not published.

### Properties

| Property       | Data Type | Constraints     | Description                          |
|----------------|-----------|-----------------|--------------------------------------|
| gis_nr         | string    | unique per year | Identifier of the usage area         |
| blw_nr         | string    | 4 digits        | Federal usage code (LNF), e.g. `0613` |
| blw_name       | string    |                 | Usage name, abbreviated              |
| flaeche        | number    | ares            | Area                                 |
| outside_canton | string    | J/N             | Field lies outside the canton        |
| farm_id        | string    |                 | Farm number                          |

Further columns: municipality (`bfsnr`, `gembez`), payment and contract flags, slope classes.
