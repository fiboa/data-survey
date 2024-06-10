# The Netherlands

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Rijksdienst voor Ondernemers (RVO) (Government)
- **Homepage:** https://www.pdok.nl/introductie/-/article/referentiepercelen
- **Homepage crop fields:** https://www.pdok.nl/introductie/-/article/basisregistratie-gewaspercelen-brp-

## Overview

Since 2011, the ministry of agriculture or associated government bodies have been publishing both 
Field Blocks (reference parcels) and Crop Fields as open data (public domain). Crop field data is
available from 2005 onwards and is typically published in july for a current year as a 
"preliminary dataset", followed-up in the next year by a permanent data set.

Crop Fields are supplied/drawn by farmers and advisors to apply for the Common Agricultural 
Policy (CAP) subsidy scheme. Additionally, the data is used for agricultural statistics and 
policymaking.

The datasets are shared as downloadable files, and the most recent ones as OGC WMS & WFS services.

## Data & Metadata

- **URL:** https://www.pdok.nl/introductie/-/article/referentiepercelen and https://www.pdok.nl/introductie/-/article/basisregistratie-gewaspercelen-brp-
- **Documentation:** https://data.overheid.nl/dataset/10674-basisregistratie-gewaspercelen--brp-
- **File Format:** GeoPackage
- **Projection:** EPSG:28992 (RD-New)
- **License:** CC0 (public domain)

The boundaries of crop fields supposed to fit within the reference parcels. The used crop classification
is a mix of pure crops, crop categories, land cover types and attributes used for specific subsidy requirements.
Currently, the publishing organization doesn't mention _crop_ but designates this attribute as _land cover_.

### Properties

The Reference Parcel dataset has the following properties:

| Property   | **Data Type** | Constraints | Description                                                                    |
|------------|---------------|-------------|--------------------------------------------------------------------------------|
| fid        | integer       |             | Identifier                                                                     |
| versiebron | string        |             | Source (digital source, e.g. aerial photo)                                     |
| type       | string        |             | Parcel type: Hout (Wood), Landbouwgrond (Arable field), Overig (Other), Water) |

Properties of Crop Fields:

| Property  | **Data Type** | Constraints   | Description                                                                                                  |
|-----------|---------------|---------------|--------------------------------------------------------------------------------------------------------------|
| fid       | integer       |               | Identifier                                                                                                   |
| category  | string        | max 100 chars | Source: Grasland (Grass land), Bouwland (Arable field), Sloot (Ditch), Landschapselement (Landscape element) |
| gewas     | string        |               | Crop description                                                                                             |
| gewascode | integer       |               | Crop identifier                                                                                              |
| jaar      | integer       |               | Year                                                                                                         |
| status    | string        | max 20 chars  | Status                                                                                                       |

### Example

See [example map](https://app.pdok.nl/viewer/#x=159472.96&y=491852.09&z=9.5964&background=BRT-A%20standaard&layers=34026fa9-603d-4511-998c-810c88cd968c;referentiepercelen,1f7d475c-179d-4c71-89ca-4b5fd210ec18;BrpGewas)

## API

Reference Parcels documentation https://www.pdok.nl/ogc-webservices/-/article/referentiepercelen

| Standard | URL                                                     |
|----------|---------------------------------------------------------|
| OGC WMS  | https://service.pdok.nl/rvo/referentiepercelen/wms/v1_0 |
| OGC WFS  | https://service.pdok.nl/rvo/referentiepercelen/wfs/v1_0 |

Crop Field documentation https://www.pdok.nl/ogc-webservices/-/article/basisregistratie-gewaspercelen-brp-

| Standard | URL                                                   |
|----------|-------------------------------------------------------|
| OGC WMS  | https://service.pdok.nl/rvo/brpgewaspercelen/wms/v1_0 |
| OGC WFS  | https://service.pdok.nl/rvo/brpgewaspercelen/wfs/v1_0 |
