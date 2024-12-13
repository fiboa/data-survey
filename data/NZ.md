# NZ National irrigated land

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** NZ Ministry for the environment
- **Homepage:** https://environment.govt.nz/

## Overview

This dataset covers Irrigated Land. It's not a full/high-quality crop field dataset for the country.

DATA SOURCE: Aqualinc Research Limited, [Technical report available](https://environment.govt.nz/publications/national-irrigated-land-spatial-dataset-2020-update)

Adapted by Ministry for the Environment and Statistics New Zealand to provide for environmental reporting transparency

The spatial data covers all mainland regions of New Zealand, with the exception of Nelson, which is not believed to 
contain significant irrigated areas. The spatial dataset is an update of the national dataset that was first 
created in 2017. The current update has incorporated data from the 2019 – 2020 irrigation season.

More information on this dataset and how it relates to our environmental reporting indicators and topics can be 
found in [the attached data quality pdf](https://data.mfe.govt.nz/services/api/v1.x/layers/105407/versions/312134/attachments/22954/download/).

Data can be downloaded manually by going to https://data.mfe.govt.nz/layer/105407-irrigated-land-area-raw-2020-update/ and clicking Export

## Data

- **URL:** https://data.mfe.govt.nz/layer/105407-irrigated-land-area-raw-2020-update/
- **Documentation:** https://environment.govt.nz/publications/national-irrigated-land-spatial-dataset-2020-update/
- **Document:** https://environment.govt.nz/assets/Publications/national-irrigated-land-spacial-dataset.pdf
- **File Format:** GeoPackage / Shapefile
- **Projection:** EPSG:2193 NZGD2000 / New Zealand Transverse Mercator 2000
- **License:** CC-BY-4.0 https://data.mfe.govt.nz/license/attribution-4-0-international/
- **Attribution:** New Zealand Ministry for the Environment

> Users of the spatial dataset are advised:
> 
> - This is a desktop study, and the methods used in the mapping cannot be relied on to give complete
> accuracy. Verification has only been carried out in a limited number of catchments, for other
> projects.
> - Before reliance is made on the spatial dataset in relation to specific catchments, irrigation schemes
> or farms, it is recommended that updated information should be sought from irrigation schemes and
> / or individual farms.

### Properties

| Property   | Data Type | Constraints | Description                                                                  |
|------------|-----------|-------------|------------------------------------------------------------------------------|
| type       | string    |             | Irrigation type. Drip/micro, Rotorainer, Pivot, K-line/Long lateral, Unknown |
| notes      | string    |             | remarks                                                                      |
| area_ha    | double    |             | area                                                                         |
| year_irr   | bigint    |             | year irrgation                                                               |
| yearmapped | bigint    |             | year mapped                                                                  |
| status     | string    |             |                                                                              |
| confidence | string    |             | Confidence of correct data; High/Low/Medium or None                          |
| Region     | string    |             | New Zealand Region                                                           |

### Example

| type                | notes                                               | area_ha        | year_irr | yearmapped | status  | confidence | Region        |
|---------------------|-----------------------------------------------------|----------------|----------|------------|---------|------------|---------------|
| Unknown             | None                                                | 0.204174327452 | 2020     | 2020       | Current | Low        | Auckland      |
| Drip/micro          | None                                                | 5.91263503012  | 2016     | 2017       | Current | Medium     | Bay of Plenty |
| Rotorainer          | None                                                | 26.4371163611  | 2013     | 2014       | Current | None       | Canterbury    |
| Solid-set           | None                                                | 1.20048255884  | 2015     | 2016       | Current | None       | Canterbury    |
| Unknown             | None                                                | 36.578878303   | 2014     | 2015       | Current | None       | Canterbury    |
| Pivot               | None                                                | 219.424475437  | 2013     | 2014       | Current | None       | Canterbury    | 
| K-line/Long lateral | None                                                | 2.26121807541  | 2015     | 2016       | Current | None       | Canterbury    |
| Drip/micro          | NDVI indicates as irrigated but there is no consent | 2.9467795853   | 2016     | 2017       | Current | Low        | Gisborne      |

## API

The services and API-keys are processed through the https://koordinates.com/ platform


| Standard    | URL                                                                                                                                                            | Documentation |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| OGC WFS     | https://data.mfe.govt.nz/services;key=[api_token]/wfs/layer-105407/?service=WFS&request=GetCapabilities                                                        | -             |
| OGC WMS     | https://data.mfe.govt.nz/services;key=[api_token]/wfs/?service=WFS&request=GetCapabilities                                                                     |               |
| Vector json | https://data.mfe.govt.nz/services/query/v1/vector.json?key=[api_token]&layer=105407&x=[x]&y=[y]&max_results=3&radius=10000&geometry=true&with_field_names=true |               |

### Example

https://data.mfe.govt.nz/layer/105407-irrigated-land-area-raw-2020-update/
