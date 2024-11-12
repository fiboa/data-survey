# Switzerland

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Konferenz der kantonalen Geoinformations- und Katasterstellen
- **Homepage:** https://www.kgk-cgc.ch/

## Overview

The cropfields of Switzerland (Nutzungsflächen) are published per administrative subdivision called Canton.
The [swiss open data portal](http://geodienste.ch/) offers 
[various ways to access these fields](https://www.geodienste.ch/services/lwb_nutzungsflaechen) .

One can filter on "Verfügbarkeit" == "Frei erhältlich" and select only the open data. That leaves out Cantons AR, NW, OW, VD and LI.
The downloaded data can be shared with a open_by license. See https://opendata.swiss/de/terms-of-use . 

> Free use. Citing the source is mandatory.
> 
> - You may use this dataset for non-commercial purposes.
> - You may use this dataset for commercial purposes.
> - A source reference is mandatory (author, title and link to the dataset).

## Data

- **URL:** https://www.geodienste.ch/services/lwb_nutzungsflaechen
- **Documentation:** https://geobasisdaten.ch/detail/818418/
- **File Format:** gpkg
- **Projection:** EPSG:2056
- **License:** Open-BY (https://opendata.swiss/de/terms-of-use)
- **License documentation:** [Nutzungsbedingungen](https://www.ag.ch/geoportal/geodatenshop/Nutzungsbedingungen.aspx?Typ=NutzungsbedingungenAGIS1)

### Properties

| Property                | Data Type | Constraints | Description     |
|-------------------------|-----------|-------------|-----------------|
| FID                     | number    |             | Identifier      |
| bezugsjahr              | number    |             | Year            |
| lnf_code                | number    |             |                 |
| nutzung                 | string    |             | Usage           |
| ist_ueberlagernd        | boolean   |             | Overlaps        |
| code_programm           | string    |             |                 |
| programm                | string    |             |                 |
| nutzungsidentifikator   | string    |             |                 |
| anzahl_baeume           | number    |             | Number of trees |
| bewirtschaftungsgrad    | number    |             |                 |
| beitragsberechtigt      | number    |             |                 |
| nutzung_im_beitragsjahr | number    |             |                 |
| nhg                     | boolean   |             |                 |
| ist_definitiv           | boolean   |             | is final        |
| verpflichtung_von       | number    |             |                 |
| verpflichtung_bis       | number    |             |                 |
| schnittzeitpunkt        | string    |             |                 |
| identifikator_be        | string    |             |                 |
| identifikator_be        | string    |             |                 |
| flaeche_m2              | int       |             | area            |
| kanton                  | string    |             | Canton code     |

### Example

An impression (with crop categories) can be seen on the swiss geoportal map: https://s.geo.admin.ch/zoa4b9lok3g8
