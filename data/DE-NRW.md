# North Rhine-Westphalia (NRW), Germany

## Submission Details

- **Submitter (Affiliation):** Matthias Mohr
- **Data Provider:** Land Nordrhein-Westfalen / Open.NRW (Government)
- **Homepage:** https://www.opengeodata.nrw.de/produkte/umwelt_klima/bodennutzung/landwirtschaft/

## Overview

A field block (German: "Feldblock") is a contiguous agricultural area surrounded by permanent boundaries, which is cultivated by one or more farmers with one or more crops, is fully or partially set aside or is fully or partially taken out of production. Field blocks are classified separately according to the main land uses of arable land, grassland, permanent crops, 2nd pillar and other. Since 2005, field blocks in NRW have represented the area reference within the framework of the Integrated Administration and Control System (IACS) for EU agricultural subsidies.

## Data & Metadata

- **URL:** https://www.opengeodata.nrw.de/produkte/umwelt_klima/bodennutzung/landwirtschaft/DGL_EPSG25832_Shape.zip
- **Documentation:**
  - https://www.geoportal.nrw/app.html?lang=de#/datasets/iso/57ba5409-f0de-4882-90b6-38660b088594
  - https://www.opengeodata.nrw.de/produkte/umwelt_klima/bodennutzung/landwirtschaft/Feature_Description_Chamber_of_Agriculture_NRW.pdf

- **File Format:** Shapefile
- **Geometry Format (if different from data):** -
- **Metadata Format (if different from data):** INSPIRE
- **Projection:** EPSG:25832 (UTM 32N)
- **License:** [Datenlizenz Deutschland Namensnennung 2.0](https://www.govdata.de/dl-de/by-2-0)

### Properties

| Property   | Data Type | Constraints     | Description                                                  |
| ---------- | --------- | --------------- | ------------------------------------------------------------ |
| ID         | integer   | 9 digits        | Internal identifier                                          |
| INSPIRE_ID | string    | 65 chars        | INSPIRE-compliant identifier. Example: `https://geodaten.nrw.de/id/inspire-lc-dgl/landcoverunit/6467974` |
| FLIK       | string    | 16 chars        | Area identifier for field blocks. Example: `DENWLI0552020444` |
| GUELT_VON  | string    | ISO date        | Valid since the given date.                                  |
| NUTZ_CODE  | string    | A, G, S, F or K | Category of land use. A = Arable land, G = Permanent grassland, S = Other land, F = Eligible in the 2nd pillar, K = Permanent Crops |
| NUTZ_TXT   | string    | see description | Textual representation of NUTZ_CODE in German (`Ackerland`, `Dauergrünland`, `Sonstige Flächen`, `Förderfähig 2. Säule`,  `Dauerkultur`) |
| AREA_HA    | number    | > 0             | Area in ha                                                   |

## API

| Standard | URL | Documentation |
| -------- | --- | ------------- |
| OGC API - Features (INSPIRE) | https://ogc-api.nrw.de/inspire-lc-fb/v1?f=json | https://ogc-api.nrw.de/inspire-lc-fb/v1/api?f=html |


The API has a slightly different naming scheme compared to the Shapefiles.

### Example

```json
{
  "type":"Feature",
  "id":607,
  "geometry":{
    "type":"Polygon",
    "coordinates":[[[8.963588166031796,51.86108459143304],[8.963332099463827,51.861166220984295],[8.963023949438366,51.86126446099501],[8.962807806023463,51.86157245469338],[8.963068779269776,51.86182317209762],[8.963205382702137,51.86199858948753],[8.963104181084756,51.862339234153104],[8.962934975707428,51.862779908349644],[8.96288730042154,51.86291106819299],[8.962787666837123,51.86320805101205],[8.962268809866147,51.86319728517804],[8.962224669862318,51.8631550385939],[8.96239137074055,51.86275329910849],[8.962453087130068,51.86258394675623],[8.962424138116727,51.862408678926926],[8.962249495307578,51.86219086406462],[8.962072367607826,51.86197873684772],[8.961876422380694,51.861773883411864],[8.96168129403757,51.86158390400363],[8.9615935274418,51.86149845835634],[8.961368301166255,51.86126749492061],[8.961328706296499,51.8612269119461],[8.961313083509012,51.86116132430056],[8.961437590200225,51.860861212861295],[8.961615195961874,51.86055753293063],[8.961635987782488,51.86053362319123],[8.961752892040964,51.86039907057983],[8.961892496440246,51.86026670915993],[8.962086880316214,51.86008241603175],[8.962272618290259,51.85992568494658],[8.96238182269965,51.859921881581315],[8.962833998198581,51.86022519148945],[8.962885022714847,51.86025943160001],[8.963102532758805,51.860432824663945],[8.963313736964306,51.86068758906699],[8.963425562179406,51.8608224546116],[8.963588166031796,51.86108459143304]]]
  },
  "properties":{
    "inspireId":"https://geodaten.nrw.de/id/inspire-lc-fb/landcoverunit/607",
    "flik":"DENWLI0541190189",
    "landCoverObservation.class.href":"https://ogc-api.nrw.de/inspire-lc-fb/v1/../../codelist/v1/collections/lcclassvalue_fb/items/A",
    "landCoverObservation.class.title":"Ackerland",
    "validFrom":"2005-02-28T00:00:00Z",
    "area_ha":2.8238
  },
  "links":[
    {
      "href":"https://ogc-api.nrw.de/inspire-lc-fb/v1/collections/landcoverunit/items/607?f=json",
      "rel":"self",
      "type":"application/geo+json",
      "title":"Dieses Dokument"
    },
    {
      "href":"https://ogc-api.nrw.de/inspire-lc-fb/v1/collections/landcoverunit/items/607?f=html",
      "rel":"alternate",
      "type":"text/html",
      "title":"Dieses Dokument als HTML"
    },
    {
      "href":"https://geodaten.nrw.de/id/inspire-lc-fb/landcoverunit/607",
      "rel":"canonical",
      "title":"Dauerhafte URI"
    },
    {
      "href":"https://ogc-api.nrw.de/inspire-lc-fb/v1/collections/landcoverunit?f=json",
      "rel":"collection",
      "type":"application/json",
      "title":"Die Datensammlung, zu der das Objekt gehört"
    }
  ]
}
```

