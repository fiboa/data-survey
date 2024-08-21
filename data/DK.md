# Denmark

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Danish Agricultural Agency, under the Ministry of Food, Agriculture and Fisheries of Denmark
- **Homepage:** https://lbst.dk/ , https://fvm.dk/

## Overview

The Danish Ministry of Food, Agriculture and Fisheries publishes different open datasets. In this context,
the relevant ones are Field Blocks (Markblokke) and Crop Fields (Marker).

Crop field data is available from 2005 onwards and is typically published as
"preliminary data" from the start of a year (updated monthly). Field blocks are available 
before the year starts, starting from 2008.

## Data

- **URL:** https://landbrugsgeodata.fvm.dk/
- **Documentation:** https://geodata-info.dk/srv/eng/catalog.search#/metadata/d91b2c99-d9b0-4e6d-b323-20ac80548186
- **Alternative open data portals**: https://sdfe.dk/ , https://www.geodata-info.dk/
- **File Format:** Shapfile (in zip)
- **Projection:** EPSG:25832
- **License:** CC-0

### Properties

| Property  | Data Type | Constraints   | Description                         |
|-----------|-----------|---------------|-------------------------------------|
| Marknr    | string    | max 200 chars | Identifier                          |
| IMK_areal | number    |               | Geometry Area                       |
| Journalnr | string    |               | Journal Number                      |
| CVR       | string    |               | Requester identifier (farmer)       |
| Afgkode   | integer   |               | Crop identifier                     |
| Afgroede  | string    |               | Crop description                    |
| GB        | number    | 0 or 1        | 1 indicates basic payment Requested |
| GBanmeldt | number    |               | Declared Area                       |
| Markblok  | string    |               | Field block identifier              |

## API

| Standard | URL                                                                                           |
|----------|-----------------------------------------------------------------------------------------------|
| OGC WFS  | https://geodata.fvm.dk/geoserver/Marker/wfs?request=GetCapabilities&service=WFS&version=1.1.0 |
| OGC WMS  | https://geodata.fvm.dk/geoserver/Marker/wms?request=GetCapabilities&service=WMS&version=1.1.0 |

### Example

See https://miljoegis.mim.dk/spatialmap?profile=lbst

