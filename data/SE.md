# Sweden Jordbruksskiften

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Jordbruksverket (The Swedish Board of Agriculture)
- **Homepage:** https://jordbruksverket.se/
- **Contact:** https://jordbruksverket.se/e-tjanster-databaser-och-appar/e-tjanster-och-databaser-stod/kartor-och-gis/kontakta-gis-supporten

## Overview

A crop field (Jordbruksskift) is a contiguous area of land within a block where a farmer grows a crop or otherwise manages the land. 
To receive compensation for agricultural support (EU support), farmers apply for support from the 
Swedish Agency for Agriculture via a SAM application. The data set contains parcels where the area 
applied for and the area decided on are the same. The data is published at the end of a year. 

The crop code list can be accessed via: https://jordbruksverket.se/stod/lantbruk-skogsbruk-och-tradgard/sam-ansokan-och-allmant-om-jordbrukarstoden/grodkoder

## Data

- **URL:** https://jordbruksverket.se/e-tjanster-databaser-och-appar/e-tjanster-och-databaser-stod/kartor-och-gis
- **Documentation:** https://inspire-geoportal.ec.europa.eu/srv/eng/catalog.search#/datasetdetails?country=se&view=IACSOverview&theme=none&resourceId=e317c48b-2a5e-4590-a2d5-c79900541d13
- **File Format:** Shape-ZIP
- **Projection:** EPSG:3006 (SWEREF 99 TM)
- **License:** Open data
- **Data Creation Details:** CAP Application data (called SAM in Sweden)

### Properties

| Property   | Data Type | Constraints | Description           |
|------------|-----------|-------------|-----------------------|
| arslager   | integer   |             | Application year      |
| blockid    | string    |             | Block identifier      |
| skiftesbet | string    |             | Crop field identifier | 
| grdkod_mar | integer   |             | Main crop code        |
| grdkod_und | integer   |             | Sub crop code         |    
| ansokt_are | float     |             | Declared area         |
| faststalld | float     |             | Determined area       | 


## API (optional)

| Standard | URL | Documentation   |
| -------- | --- |-----------------|
| OGC WMS  | https://epub.sjv.se/inspire/inspire/ows?request=getcapabilities&service=wms&version=1.3.0 | -               |
