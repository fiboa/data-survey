# California Statewide Crop Mapping

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** California Department of Water Resources
- **Homepage:** https://water.ca.gov/

## Overview

For many years, the California Department of Water Resources (DWR) has collected land use data throughout the state
and used this information to develop water use estimates for statewide and regional planning efforts, including water
use projections, water use efficiency evaluation, groundwater model development, and water transfers. These data are
essential for regional analysis and decision making, which has become increasingly important as DWR and other state agencies
seek to address resource management issues, regulatory compliance issues, environmental impacts, ecosystem services,
urban and economic development, and other issues. Increased availability of digital satellite imagery, aerial photography
and new analytical tools make remote sensing based land use surveys possible at a field scale that is comparable to that
of DWR’s historical on the ground field surveys. Current technologies allow accurate, large-scale crop and land use
identification to be performed at desired time increments, and make possible more frequent and comprehensive statewide
land use information. Responding to this need, DWR sought expertise and support for identifying crop types and other
land uses and quantifying crop acreages statewide using remotely sensed imagery and associated analytical techniques.
Currently, Statewide Crop Maps are available for the Water Years 2014, 2016, 2018, 2019, 2020, 2021 and PROVISIONALLY 
for 2022.

## Data & Metadata

- **URL:** https://data.cnra.ca.gov/dataset/6c3d65e3-35bb-49e1-a51e-49d5a2cf09a9/resource/35251d3a-22ce-4661-9e11-4eecd0edebd1/download/i15_crop_mapping_2022_provisional_shp.zip 
- **URL:** https://data.cnra.ca.gov/dataset/statewide-crop-mapping/resource/6ade4f9e-3631-4666-b2d9-21cf20222a6e
- **Documentation:** https://lab.data.ca.gov/dataset/statewide-crop-mapping
- **Documentation:** https://data.cnra.ca.gov/dataset/statewide-crop-mapping
- **File Format:** Shapefile/zip and ESRI FileGDB
- **Projection:** EPSG:4269 (NAD83)
- **License:** CC-0

### Properties

| Property     | **Data Type** | Constraints | Description    |
|--------------|---------------|-------------|----------------|
| DataStatus   | String        | length=11   |                |
| UniqueID     | String        | length=80   | Identifier     |
| DWR_REVISE   | String        | length=1    |                |
| SYMB_CLASS   | String        | length=2    |                |
| MULTIUSE     | String        | length=1    |                |
| CLASS1       | String        | length=2    |                |
| SUBCLASS1    | String        | length=7    |                |
| SPECOND1     | String        | length=1    |                |
| IRR_TYP1PA   | String        | length=1    |                |
| IRR_TYP1PB   | String        | length=1    |                |
| PCNT1        | String        | length=2    |                |
| CLASS2       | String        | length=2    |                |
| SUBCLASS2    | String        | length=7    |                |
| SPECOND2     | String        | length=1    |                |
| IRR_TYP2PA   | String        | length=1    |                |
| IRR_TYP2PB   | String        | length=1    |                |
| PCNT2        | String        | length=2    |                |
| CLASS3       | String        | length=2    |                |
| SUBCLASS3    | String        | length=7    |                |
| SPECOND3     | String        | length=1    |                |
| IRR_TYP3PA   | String        | length=1    |                |
| IRR_TYP3PB   | String        | length=1    |                |
| PCNT3        | String        | length=2    |                |
| CLASS4       | String        | length=2    |                |
| SUBCLASS4    | String        | length=7    |                |
| SPECOND4     | String        | length=1    |                |
| IRR_TYP4PA   | String        | length=1    |                |
| IRR_TYP4PB   | String        | length=1    |                |
| PCNT4        | String        | length=2    |                |
| UCF_ATT      | String        | length=37   |                |
| YR_PLANTED   |               |             |                |   
| SEN_CROP     | String        | length=4    |                |
| ADOY_SEN     |               |             |                |   
| CROPTYP1     | String        | length=4    |                |
| ADOY1        |               |             |                |   
| CROPTYP2     | String        | length=4    |                |
| ADOY2        |               |             |                |   
| CROPTYP3     | String        | length=4    |                |
| ADOY3        |               |             |                |   
| CROPTYP4     | String        | length=4    |                |
| ADOY4        |               |             |                |   
| EMRG_CROP    | String        | length=4    |                |
| ADOY_EMRG    |               |             |                |   
| REGION       | String        | length=4    |                |
| ACRES        |               |             |                |   
| COUNTY       | String        | length=80   | County         |
| HYDRO_RGN    | String        | length=17   | Hydro Region   |
| LIQ_REPORT   | String        | length=20   |                |
| MAIN_CROP    | String        | length=4    | Main Crop code |
| MAIN_CROP_   |               |             |                |   
| WO1_FREQUE   | String        | length=7    |                |


### Example

Historic County Land Use Surveys spanning 1986 - 2015 may also be accessed using the CADWR Land Use 
Data Viewer: https://gis.water.ca.gov/app/CADWRLandUseViewer. For Regional Land Use Surveys follow:
https://data.cnra.ca.gov/dataset/region-land-use-surveys. 
For County Land Use Surveys follow: https://data.cnra.ca.gov/dataset/county-land-use-surveys.

# API

As published at [the documentation](https://lab.data.ca.gov/dataset/statewide-crop-mapping).

| Standard | URL                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| OGC WMS  | https://utility.arcgis.com/usrsvcs/servers/af03260dc1304199aca6fb9109a8f900/rest/services/Planning/i15_Crop_Mapping_2022_Provisional/MapServer |
| OGC WMS  | https://utility.arcgis.com/usrsvcs/servers/5fe15fbb9296403eb4ea91e3d031619d/rest/services/Planning/i15_Crop_Mapping_2021/MapServer             |


