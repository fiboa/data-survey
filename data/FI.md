# Finnish Crop Fields (Maatalousmaa)

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Finnish Food Authority
- **Homepage:** https://www.ruokavirasto.fi/en/about-us/open-information/spatial-data-sets/

## Overview

The Finnish Food Authority (FFA) since 2020 produces spatial data sets, 
more specifically in this context the "Field parcel register" and "Agricultural parcel containing spatial data". 
A set called "Agricultural land: arable land, permanent grassland or permanent crop (land use)".

All spatial data sets can be viewed in Finland’s national geo-portal [Paikkatietoikkuna](https://kartta.paikkatietoikkuna.fi/?lang=en).

## Data

- **URL:** https://download.inspire.ruokavirasto-awsa.com/data/2023/LandUse.ExistingLandUse.AgriculturalArea.gpkg
- **Documentation:** https://www.ruokavirasto.fi/en/about-us/open-information/spatial-data-sets/
- **File Format:** GeoPackage
- **Projection:** EPSG:3067
- **License:** CC-BY-4.0

### Properties

| Property             | Data Type  | Constraints | Description                |
|----------------------|------------|-------------|----------------------------|
| fid                  | int        |             |                            |
| VUOSI                | int        |             | Year                       |
| PERUSLOHKOTUNNUS     | int        |             | Official Identifier        |
| LOHKONUMERO          | int        |             | Field block Identifier     |
| PINTA_ALA            | float      |             | Surface Area               |
| KASVIKOODI           | int        |             | Crop code                  |
| KASVIKOODI_SELITE_FI | string     |             | Crop description (Finnish) |
| KASVIKOODI_SELITE_SV | string     |             | Crop description (Swedish) |

License info: https://www.ruokavirasto.fi/en/about-us/open-information/spatial-data-sets/ - Creative Commons BY 4.0

### Example

Example field from 2022:

```
    fid: 279790
    VUOSI: 2022
    PERUSLOHKOTUNNUS: 2330949709
    LOHKONUMERO: 2
    PINTA_ALA: 10,36
    KASVIKOODI: 1400
    KASVIKOODI_SELITE_FI: Kaura
    KASVIKOODI_SELITE_SV: Havre
```

## API

| Standard | URL                                                                         |
|----------|-----------------------------------------------------------------------------|
| OGC WMS  | https://inspire.ruokavirasto-awsa.com/geoserver/wms?request=getcapabilities |
| OGC WFS  | https://inspire.ruokavirasto-awsa.com/geoserver/wfs?request=getcapabilities |

Data is also discoverable through the [Spatial directory](https://www.paikkatietohakemisto.fi/geonetwork/srv/eng/catalog.search#/search?resultType=details&sortBy=relevance&any=Ruokavirasto)
