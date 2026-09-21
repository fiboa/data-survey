# Poland

## Submission Details

- **Submitter (Affiliation):** Saidy Barry, moreGeo GmbH
- **Data Provider (Legal Entity):** Agencja Restrukturyzacji i Modernizacji Rolnictwa (ARiMR, the paying agency) (Government)
- **Homepage:** https://geoportal.arimr.gov.pl/mapy/apps/sites/#/portal

## Overview

ARiMR runs the Polish IACS and publishes two kinds of spatial data on its geoportal, both without an
account:

- **Declared crops** ("Uprawy rolne deklarowane GSA"): the agricultural parcels farmers declared in
  their geospatial aid applications, one layer per campaign year (2025, 2026), about 10.7 million
  parcels each, with the declared crop as a Polish name, a crop group, the support schemes the parcel
  was declared under, and the declared area. These layers exist only on the WFS.
- **LPIS reference data**: the reference parcels, which in Poland are the cadastral parcels, the
  land-cover objects with a class, and the maximum eligible area per parcel (MKO JPO), as WFS/WMS and
  as one shapefile per voivodeship. Only the current state is published.

No layer carries a farmer, application or parcel identifier; the LPIS layers carry the cadastral
parcel identifier.

## Data

- **URL:** Declared crops: https://geoportal-w2.arimr.gov.pl/geoserver/gsa_public/wfs (WFS);
  LPIS: https://geoportal-w1.arimr.gov.pl/geoserver/lpis_public/wfs (WFS) and
  https://geoportal.arimr.gov.pl/mapy/sharing/rest/content/items/<item id>/data (shapefiles, ids below)
- **Documentation:** https://www.gov.pl/web/arimr/system-identyfikacji-dzialek-rolnych-lpis;
  the item descriptions on the geoportal; the WFS capabilities of the two endpoints above
- **File Format:** WFS 2.0/1.1.0 (GML, GeoJSON, zipped Shapefile, CSV); LPIS also as zipped Shapefiles
- **Projection:** EPSG:2180 (ETRS89 / Poland CS92)
- **License:** Not stated. The items are tagged "Publiczne dane ARIMR" and download without an account,
  but neither the items nor the WFS capabilities carry a licence. Contact: geoportal_hd@arimr.gov.pl
- **Data Creation Details:** Official IACS records: the declarations submitted by farmers; the LPIS
  maintained from orthophotos, state registers and controls

### Declared crops

| Layer | Content | 2025 | 2026 |
| --- | --- | ---: | ---: |
| `uprawy_rolne_<year>` | all declared parcels with their crop | 10,764,131 | 10,654,363 |
| `uprawy_na_gruntach_ornych_<year>` | the parcels on arable land | 7,350,566 | 7,149,264 |
| `uprawy_tuz_<year>` | the permanent grassland (TUZ) | 2,879,917 | 2,977,904 |
| `prow_onw_<year>`, `prow_prsk_<year>`, `prow_re_<year>`, `prow_wzl_<year>` | parcels declared under the rural development schemes ONW, PRSK/ZRSK, RE, WZL | 6.3 M, 0.3 M, 0.2 M, 13 k | 6.2 M, 0.4 M, 0.3 M, – |

Feature counts as reported by the WFS on 2026-09-21.

| Property | Data Type | Constraints | Description |
| -------- | --------- | ----------- | ----------- |
| geometry | Polygon | EPSG:2180 | Declared agricultural parcel |
| roslina | string | Polish crop name, 701 distinct over both campaigns | Declared crop, e.g. `pszenica zwyczajna ozima`, `TUZ`, `Sad`, `ugór` |
| roslina_skrocona | string | 302 distinct | Shortened crop name, e.g. `pszenica ozima` |
| grupa_roslin | string | comma-joined | Crop group(s), e.g. `zboża`, `użytki zielone`, `pastewne`, `sady plantacje trwałe`, `warzywa` |
| gr_upraw | string | comma-joined codes, may be empty | Support schemes the parcel was declared under, e.g. `PWD`, `UPP`, `ONW`, `RE2327` (not expanded by ARiMR) |
| pow | string | `"<n.nn> ha"` | Declared area in hectares |

Example (`uprawy_rolne_2026`):

| roslina | roslina_skrocona | grupa_roslin | gr_upraw | pow |
| --- | --- | --- | --- | --- |
| pszenica zwyczajna ozima | pszenica ozima | zboża | PWD,UPP | 0.79 ha |
| TUZ | tuz | użytki zielone | ONW,PWD | 1.35 ha |

Access: at most 50,000 features per request, paged with `startIndex`. Use WFS 1.1.0 on the workspace
endpoint above; WFS 2.0 does not answer on the large layers, and the per-layer endpoints of the two
largest refuse connections. Zipped shapefiles need `format_options=CHARSET:UTF-8` and carry no feature id.

### LPIS reference data

| Layer | Content | Features | Shapefiles |
| --- | --- | ---: | --- |
| `dzialki_referencyjne` | reference parcels (cadastral parcels) | 37,128,715 | 16 zips, 3.7 GB |
| `pokrycie_terenu_wfs` | land-cover objects with a class | 34,902,547 | 16 zips, 5.2 GB |
| `mko_jpo` | maximum eligible area per parcel | 13,131,953 | 16 zips, 1.9 GB |

Feature counts as reported by the WFS on 2026-09-19; this WFS returns at most 9,999 features per
request. The shapefiles hold the current state and are refreshed weekly; the generation date is the
date of the files inside the zip. An eligible area can be a MultiPolygon. About half of the
land-cover records have no geometry.

| Property | Data Type | Constraints | Description |
| -------- | --------- | ----------- | ----------- |
| id_ewidenc | string | unique; `WWPPGG_R.OOOO.[AR_NR.].NR_DZ` | Cadastral parcel identifier; the first two digits are the voivodeship (TERYT = ISO 3166-2:PL) |
| powierzchn | string | `"<integer> m2"` | Area in m² |
| typ (land cover only) | string | 12 codes | CU, S, T, O, L, Z, W, ZS, OM, OW, R, `D,K,U,I,P`; legend in the item description |

The shapefile items and their ids are listed by the portal search, e.g. the 16 MKO JPO files (32–238 MB
each) by https://geoportal.arimr.gov.pl/mapy/sharing/rest/search?q=MKO%20type:%22Shapefile%22&f=json and
all LPIS items by https://geoportal.arimr.gov.pl/mapy/sharing/rest/search?q=LPIS&f=json.

## API

| Standard | URL | Documentation |
| -------- | --- | ------------- |
| OGC WFS (declared crops, 14 layers) | https://geoportal-w2.arimr.gov.pl/geoserver/gsa_public/wfs | 50,000 features per request |
| OGC WFS (LPIS, 16 layers) | https://geoportal-w1.arimr.gov.pl/geoserver/lpis_public/wfs | 9,999 features per request |
| OGC WMS (LPIS) | https://geoportal-w1.arimr.gov.pl/geoserver/lpis_public/<layer>/wms | - |
