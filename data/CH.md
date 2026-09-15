# Switzerland

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Konferenz der kantonalen Geoinformations- und Katasterstellen (Government — association of cantonal geo-information and cadastral offices)
- **Homepage:** https://www.kgk-cgc.ch

## Overview

The crop fields of Switzerland ("Nutzungsflächen") are published per administrative subdivision (Canton) and
aggregated through the Swiss geoservices portal. Each canton declares the agricultural use of plots used as the
basis for direct payments under the Swiss agricultural policy (the federal counterpart to the EU CAP).

## Data

- **URL:** One GeoPackage per canton. The links and each canton's availability are listed in https://www.geodienste.ch/info/services.json?base_topics=lwb_nutzungsflaechen and as the `geopackage_zip` asset of the STAC items at https://www.geodienste.ch/stac/collections/lwb_nutzungsflaechen/items .
- **Documentation:** https://www.geodienste.ch/services/lwb_nutzungsflaechen and https://geobasisdaten.ch/detail/818418/
- **File Format:** GeoPackage
- **Projection:** EPSG:2056 (CH1903+ / LV95)
- **License:** [opendata.swiss terms of use](https://opendata.swiss/en/terms-of-use) (open_by — free use with mandatory source citation)

Only the current state is published, there are no earlier years. Availability differs per canton and is listed in `services.json`; BS ships an empty file, its data is included in the BL file.

The `ist_ueberlagernd` flag marks overlapping landscape elements that would otherwise duplicate the area.

### Properties

| Property                | Data Type | Constraints | Description     |
|-------------------------|-----------|-------------|-----------------|
| FID                     | number    |             | Identifier      |
| bezugsjahr              | number    |             | The year of validity |
| lnf_code                | number    |             |                 |
| nutzung                 | string    |             | Usage           |
| ist_ueberlagernd        | boolean   |             | Overlaps        |
| code_programm           | string    |             |                 |
| programm                | string    |             |                 |
| nutzungsidentifikator   | string    |             | Usage identifier |
| anzahl_baeume           | number    |             | Number of trees |
| bewirtschaftungsgrad    | number    |             | Degree to which the field is getting cultivated |
| beitragsberechtigt      | number    |             |                 |
| nutzung_im_beitragsjahr | number    |             |                 |
| nhg                     | boolean   |             |                 |
| ist_definitiv           | boolean   |             | is final        |
| verpflichtung_von       | number    |             |                 |
| verpflichtung_bis       | number    |             |                 |
| schnittzeitpunkt        | string    |             |                 |
| identifikator_be        | string    |             |                 |
| flaeche_m2              | int       |             | area in sq. meter |
| kanton                  | string    |             | Canton code     |

### Example

An impression (with crop categories) can be seen on the Swiss geoportal map: https://s.geo.admin.ch/zoa4b9lok3g8
