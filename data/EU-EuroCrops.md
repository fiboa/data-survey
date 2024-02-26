# EuroCrops

## Submission Details

- **Submitter (Affiliation):** Matthias Mohr
- **Data Provider (Legal Entity):** Maja Schneider, TUM (Individual)
- **Homepage:** https://www.eurocrops.tum.de

## Overview

EuroCrops is a dataset collection combining all publicly available self-declared crop reporting datasets from countries of the European Union. The following countries are covered:

- [Austria](https://github.com/maja601/EuroCrops/wiki/Austria)
- [Belgium](https://github.com/maja601/EuroCrops/wiki/Belgium)
- [Czechia](https://github.com/maja601/EuroCrops/wiki/Czechia)
- [Germany](https://github.com/maja601/EuroCrops/wiki/Germany)
- [Denmark](https://github.com/maja601/EuroCrops/wiki/Denmark)
- [Estonia](https://github.com/maja601/EuroCrops/wiki/Estonia)
- [Spain](https://github.com/maja601/EuroCrops/wiki/Spain)
- [France](https://github.com/maja601/EuroCrops/wiki/France)
- [Croatia](https://github.com/maja601/EuroCrops/wiki/Croatia)
- [Lithuania](https://github.com/maja601/EuroCrops/wiki/Lithuania)
- [Latvia](https://github.com/maja601/EuroCrops/wiki/Latvia)
- [Netherlands](https://github.com/maja601/EuroCrops/wiki/Netherlands)
- [Portugal](https://github.com/maja601/EuroCrops/wiki/Portugal)
- [Romania](https://github.com/maja601/EuroCrops/wiki/Romania)
- [Sweden](https://github.com/maja601/EuroCrops/wiki/Sweden)
- [Slovenia](https://github.com/maja601/EuroCrops/wiki/Slovenia)
- [Slovakia](https://github.com/maja601/EuroCrops/wiki/Slovakia)

## Data

- **URL:**
  - Shapes: https://syncandshare.lrz.de/getlink/fiAD95cTrXbnKMrdZYrFFcN8/
  - Metadata: https://zenodo.org/records/10118572
  - Cloud Native Geo Version: https://beta.source.coop/repositories/cholmes/eurocrops/

- **Documentation:** https://github.com/maja601/EuroCrops
- **File Format:** various (see below)
- **Geometry Format (if different from data):**
  - Shapefile
  - GeoJSON (MultiPolygon)
  - GeoParquet, Flatgeobuf and PMTiles single file harmonized only versions on source cooperative.

- **Metadata Format (if different from data):**
  - Shapefile (see properties below)
  - HDF5 (Sentinel-2 reflectance. Rows: Parcel ID, Columns: Timestamps, Cells: Reflectances per Band)
  - CSV (Parcel ID, HCAT ID, crop name)
  - GeoJSON (NUTS ID, crop name, crop ID, country name, ...)

- **Projection:** EPSG:4326 (GeoJSON), ... (Shapefile), ... (HDF5)
- **License:** CC-BY-SA-4.0

EuroCrops delivers mostly the source data and harmonizes the crop classification.

### Properties

The properties in the Shapefiles correspond to the source datasets from the individual countries, and adds the properties for the Hierarchical Crop and Agriculture Taxonomy (HCAT). The properties for the individual countries are described either here in the survey repo or in the wiki page of EuroCrops (see the list of countries above).

| Property   | Data Type | Constraints | Description                                                 |
| ---------- | --------- | ----------- | ----------------------------------------------------------- |
| EC_trans_n | string    | see HCAT    | The original crop name translated into English              |
| EC_hcat_n  | string    |             | The machine-readable HCAT name of the crop                  |
| EC_hcat_c  | string    | digits only | The 10-digit HCAT code indicating the hierarchy of the crop |

As noted above, each individual country has many more attributes, as they are sourced from different national sources. In the ['cloud native' versions](https://beta.source.coop/cholmes/eurocrops/) 
the only attributes included are the three above, plus the geometry, and all countries are combined into a single file.

## API

EuroCrops is made available by multiple third-parties through their APIs, e.g. Sentinel Hub and Euro Data Cube.

