# Ireland

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper; LPIS section Saidy Barry, moreGeo GmbH
- **Data Provider (Legal Entity):** Department of Agriculture, Food and the Marine (DAFM) (Government)
- **Homepage:** https://www.gov.ie/en/organisation/department-of-agriculture-food-and-the-marine/

## Overview

DAFM, the Irish paying agency, publishes the parcels of its Land Parcel Identification System (LPIS)
in two forms, both CC-BY-4.0 and without an account:

- **INSPIRE GSAA** ("Geospatial Aid Application"): the parcels claimed under area-based CAP schemes
  with the crops claimed on them, one GML file per campaign year, currently 2022–2024. Plain parcel
  identifiers.
- **Anonymous LPIS and N&P**: every LPIS parcel, claimed or not, with the crop, the digitised,
  eligible and claimed area and the commonage share, one dataset per campaign year on data.gov.ie:
  2017–2022 and 2025. Parcel and herd identifiers are hashed.

The two describe the same parcels: 19,976 of 20,000 GSAA 2022 parcels sampled have an LPIS 2022 parcel
with the same geometry. The hashed LPIS identifiers cannot be joined to the plain GSAA ones. 2023 and 2024
exist only as GSAA.

## Declared parcels (INSPIRE GSAA)

The dataset represents the outline shape of LPIS parcels as claimed under area-based schemes within the
EU Common Agricultural Policy (CAP) and the Integrated Administration and Control System (IACS). It
includes the crops claimed as part of the annual GSAA, collected through the beneficiary declaration.

### Data

- **URL:** Per-year GML downloads at `https://dafm-inspire-atom.s3.eu-west-1.amazonaws.com/files/LU/GSAA_<YEAR>.zip` for 2022–2024 (e.g. https://dafm-inspire-atom.s3.eu-west-1.amazonaws.com/files/LU/GSAA_2024.zip containing `GSAA_2024.gml`, layer `ExistingLandUseObject`); 2016–2021 and 2025 answer 403
- **Documentation:** https://inspire-geoportal.ec.europa.eu/srv/eng/catalog.search#/extenddetails?country=ie&view=priorityOverview&theme=none&resourceId=IACSdata_INSPIRE_ATOM
- **File Format:** GML (zipped), INSPIRE ELU theme
- **Projection:** EPSG:4258 (ETRS89)
- **License:** [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/)
- **Attribution:** "Ireland Department of Agriculture, Food and the Marine"

The source `crop_name` may contain multiple comma-separated crops. Rows with `crop_name == "Void"`
denote non-agricultural areas. `localId` repeats where a parcel is declared more than once.

### Properties

| Property              | Data Type | Constraints | Description   |
|-----------------------|-----------|-------------|---------------|
| localId               | int       |             | Parcel identifier |
| crop_name             | string    |             | Name(s) of the crop |
| observationDate       | datetime  |             | Date observed |
| validFrom             | datetime  |             | Date start    |

## Anonymous LPIS and N&P

### Data

- **URL:** One dataset per year on data.gov.ie: `https://data.gov.ie/dataset/anonymous-lpis-and-n-p-for-<year>` (2017–2021), `…/anonymous-lpis-data-for-2022`, `…/anonymous-lpis-data-for-2025`; the files download from `https://opendata.agriculture.gov.ie/dataset/<dataset id>/resource/<resource id>/download/<file>`
- **Documentation:** `data_fields.xlsx` in each dataset lists the fields
- **File Format:** zipped Shapefiles (Parcels, Exclusions); 2025 zipped GeoPackages (Parcels, Subfeatures)
- **Projection:** EPSG:2157 (Irish Transverse Mercator)
- **License:** [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/)

A row is a claim on a parcel and carries the parcel's geometry: 1.36–1.51 million rows on 1.31–1.42
million parcels per year for 2017–2022. Parcels claimed by several herds or split into several crops
repeat. Each parcels zip holds two shapefiles, the first at the 2 GiB DBF limit; the 2025 GeoPackage adds
3.4 million geometries without any attribute. The Exclusions file holds the ineligible features inside
parcels (scrub, roads, streams, buildings), whose deduction gives the eligible area.

### Properties

| Property | Data Type | Constraints | Description |
| -------- | --------- | ----------- | ----------- |
| geometry | Polygon | EPSG:2157 | The gross parcel |
| PARC_LAB | string | hashed, repeats per claim | Parcel label (2025: `par_lab`) |
| APP_HERD | string | hashed | Applicant's herd number (2025: `app_herd`) |
| DIGIT_AREA | number | hectares, equals the geometry area | Digitised area (2025: `digitised`) |
| MEA | number | hectares, ≤ DIGIT_AREA, may be null | Maximum eligible area (2025: `eh_area`) |
| CLAIM_AREA | number | hectares, per claim | Claimed area (2025: `claim_area`) |
| CROP_DESC | string | 223 names over all years | Declared crop or land use, e.g. `Permanent Pasture`, `Barley - Spring`, `Building` (2025: `crop`) |
| COM_IND | string | `Y`/`N` | Commonage (2025: `commonage_ind`) |
| SUB_DIV | string | 1–7, mostly null | Subdivision of a parcel into crops (2025: `sub_div`) |

The remaining columns are scheme indicators and the holding's nitrates and phosphates (N&P), repeated
on every parcel.
