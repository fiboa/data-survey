# Ireland Geospatial aid application (GSAA) dataset

## Submission Details

- **Data Provider (Legal Entity):** Ireland Department of Agriculture, Food and the Marine
- **Submitter (Affiliation):** Ivor Bosloper
- **Homepage:** https://inspire.geohive.ie/geoportal/

## Overview

Ireland INSPIRE Geospatial aid application (GSAA) dataset

This data represents the outline shape of LPIS parcels as claimed under area based schemes. The dataset includes the crops claimed as part of the annual GSAA. 
Yearly information provided through the beneficiary declaration.

## Data

- **URL:** https://osi-inspire-atom.s3-eu-west-1.amazonaws.com/IACSdata/IACS_GSAA_2022.zip
- **Documentation:** https://inspire-geoportal.ec.europa.eu/srv/eng/catalog.search#/extenddetails?country=ie&view=priorityOverview&theme=none&resourceId=IACSdata_INSPIRE_ATOM
- **File Format:** GML-zip
- **Projection:** EPSG:4258
- **License:** CC-BY-4.0
- **Contact:** info@agriculture.gov.ie

### Properties

| Property              | Data Type | Constraints | Description   |
|-----------------------|-----------|-------------|---------------|
| localId               | int       |             | Identifier    |
| crop_name             | string    |             | Name of crop  |
| observationDate       | datetime  |             | Date observed |
| validFrom             | datetime  |             | Date start    |
