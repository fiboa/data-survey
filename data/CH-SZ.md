# Schwyz, Switzerland

## Submission Details

- **Submitter (Affiliation):** Saidy Barry, moreGeo GmbH
- **Data Provider (Legal Entity):** Kanton Schwyz, Amt für Landwirtschaft (Government)
- **Homepage:** https://www.sz.ch/landwirtschaft

## Overview

The usage areas ("Landwirtschaftliche Nutzungsflächen") of the canton of Schwyz for the payment years 2022 to
2024, one WFS layer per year in a reduced form of the federal model: a multipart field is one feature per part
with the same identifier, and only code, name and the field's total area are published. The current year is on
[geodienste.ch](CH.md) in the full model with different identifiers.

## Data

- **URL:** https://map.geo.sz.ch/mapserv_proxy (WFS 2.0), layers `ms:ch.sz.a002a.nutzung.2022`, `.2023`, `.2024`; a whole year in one request with `COUNT=50000`
- **Documentation:** geocat record per layer, e.g. https://www.geocat.ch/geonetwork/srv/ger/catalog.search#/metadata/16014001-f760-4cd0-a3ed-49e2fff04856 (2024)
- **File Format:** WFS, GML 3.2 output only
- **Projection:** EPSG:2056 (CH1903+ / LV95)
- **License:** [Open Data-Lizenz für Geodienste & Geodaten des Kantons Schwyz](https://www.geodienste.ch/pdfs/SZ/lwb_nutzungsflaechen/data/Open%20Data%20Lizenz%20AFL.pdf): free use including commercial use, the licence has to be passed on with the data
- **Attribution:** "Amt für Landwirtschaft (AFL), Kanton Schwyz"

Features per year: 31,007 (2022), 31,910 (2023), 32,209 (2024). In 2024, 1,033 identifiers appear on 2,413 rows,
the parts of multipart fields; the parts' areas add up to `groesse`, which is in ares.

### Properties

| Property   | Data Type | Constraints                      | Description                          |
|------------|-----------|----------------------------------|--------------------------------------|
| nutzungsid | string    | repeated for the parts of a field | Identifier of the usage area        |
| nutzart_co | string    | 4 digits                         | Federal usage code (LNF), e.g. `0613` |
| nutzart    | string    | German                           | Usage name                           |
| groesse    | string    | ares                             | Area of the whole field              |
