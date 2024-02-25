# Title Open Supply Hub Production Points

## Submission Details

- **Submitter (Affiliation):** Kate Chapman, Open Supply Hub
- **Data Provider (Legal Entity):** Open Supply Hub
- **Homepage:** https://opensupplyhub.org/

## Overview

Open Supply Hub is building a dataset of all the supply chain production points in the world. Each point is given a unique ID and we perform matching using machine learning and data moderators to deduplicate this data. This can be done through bulk upload via spreadsheet or API. We do not consider field boundaries to be in scope for our dataset, but would like to integrate with such data. 

https://info.opensupplyhub.org/developer-resources

## Data

<!-- Any important information about your field boundary data and metadata,
e.g. in which format and projection the geometry is provided. -->

- **URL:** https://opensupplyhub.org/ (can be downloaded here)
- **Documentation:** https://info.opensupplyhub.org/developer-resources
- **File Format:** JSON or CSV
- **Geometry Format (if different from data):** Latitude/Longitude
- **Metadata Format (if different from data):** 
- **Projection:** EPSG:4326/...
- **License:** CC-BY-SA
- **Data Creation Details:** Crowdsourced primarily from brands and production points themselves
- **Computer Vision / AI Details:** We use the Python dedup library to match based on text submissions. 

...

### Properties

| Property             | Data Type | Constraints | Description                          |
| ---------------------| --------- | ----------- | -------------------------------------|
| od_id                | string    |             | a unique id for the production point |
| contribution_date    | date      |             | date of contrbution                  |
| name                 | string    |             | facility name                        |
| address              | string    |             | facility address                     | 
| country_code         | string    |             | country code                         |
| country_name         | string    |             |  country name                        |
| lat                  | decimal   |             | latitude                             |
| lng                  | decimal   |             | longitude                            |
| sector               | string    |             | sector                               |
| contributor (list)   | string    |             | all the sources of data contributions|
| number_of_workers    | string    |             | range of the number of workers       |
| parent_company       |           |             | owner of facility                    |
| processing_type      | string    |             | what processes happen there          |
| product_type         | string    |             | what types of products are made      |
| is_closed            | boolean   |             | is the facility open/closed          |
### Example

<!-- Please provide a link to the data or embed it into this document as a code block. -->

## API (optional)

<!-- Any important information about your API that is not captured in the chapters above,
e.g. an example response of a field boundary. -->

### Example

<!-- Please provide a link to the data or embed it into this document as a code block. -->
