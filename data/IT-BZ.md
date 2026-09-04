# South Tyrol (BZ), Italy

## Submission Details

- **Submitter (Affiliation):** Saidy Barry, moreGeo GmbH
- **Data Provider (Legal Entity):** Autonome Provinz Bozen – Südtirol / Provincia autonoma di Bolzano – Alto Adige (Government)
- **Homepage:** https://agricoltura.provincia.bz.it/it/home

## Overview

The utilised agricultural area of the autonomous province of Bolzano, published as a single open
layer. The dataset lineage attributes it to the province's LAFIS system and describes the polygons
as digitised manually from orthophotos or GPS survey, then *"aggregata secondo il tipo di coltura,
protezione della coltura e dettaglio di specifici tipi di coltura"* — aggregated by crop type, crop
protection and crop-type detail. Each feature is a single-part polygon with exactly one crop code,
and the schema holds no farm or parcel identifier, so a feature is an area of one crop type rather
than one farmer's application parcel.

147,743 fields covering 207,231 ha, at a median of 0.29 ha. Each carries a crop code from the
provincial code list, with the crop name in Italian and German.

## Data

- **URL:** https://geoservices6.civis.bz.it/geoserver/p_bz-Agriculture/ows
- **Documentation:** https://data.civis.bz.it/dataset/superficie-agricola-utilizzata
- **File Format:** GeoJSON, GML 2/3.1/3.2, CSV, KML and zipped Shapefile, all via WFS
- **Projection:** EPSG:25832 (ETRS89 / UTM zone 32N), declared as `ETRS89/ETRS-TM32`
- **License:** [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/deed.it), from the
  catalogue record (`license_id: cc-zero`). The WFS capabilities state no fees or access
  constraints, so the catalogue record is the citable source
- **Attribution:** © Autonome Provinz Bozen – Südtirol

The layer is `p_bz-Agriculture:Fields-Used` (identifier `p_bz:Agriculture:Fields-Used`), titled
*Landwirtschaftlich genutzte Fläche / Superficie agricola utilizzata*, covering 10.29–12.51 E,
46.18–47.14 N. The workspace holds eight further layers, none of them this dataset's fields; the
closest, `AgricultureDomains` (*Demanio provinciale: superfici agricole*), repeats this schema for
719 parcels of province-owned farmland and is a separate dataset with no ID overlap.

**The whole layer is one snapshot.** `BEGIN_DATE`, `END_DATE` and `LAST_MODIFY` each hold a single
distinct value across all rows — `2025-07-28Z`, `9999-12-31Z` and `2025-09-03Z`. There is no history
and no year variant to select.

### Properties

| Property | Data Type | Constraints | Description |
| --- | --- | --- | --- |
| `ID` | integer | required, unique | Serial identifier |
| `CODE` | string | required | Crop code from the provincial code list, e.g. `AA13`. 100 distinct values |
| `DESCRIPTION_IT` / `DESCRIPTION_DE` | string | required | Crop name in Italian and German, e.g. `Patata da consumo` / `Speisekartoffeln`. The feature type declares the Italian column of each bilingual pair first |
| `CULT_PROT_IT` / `CULT_PROT_DE` | string | 93.7% null | Crop protection. The only value present is `Rete antigrandine` / `Hagelnetz` — hail net — on 9,274 rows |
| `LSP_CODE` | string | 93.3% null | Biodiversity designation, `DIP28_1`…`DIP28_10`, on 9,921 rows. Overlays the crop rather than replacing it |
| `LSP_DESC_IT` / `LSP_DESC_DE` | string | 93.3% null | Label for `LSP_CODE`, e.g. `Prati magri e prati a torbiera bassa`, one per code |
| `AREA` | integer | required | Area in **m²** — the geometry area rounded to the nearest m², not an eligibility-adjusted figure |
| `BEGIN_DATE`, `END_DATE`, `LAST_MODIFY` | date | constant | See above; one distinct value each |
| `USER` | string | constant | Loading process, `--AF_ETL_IMPORT--` |
| `geometry` | Polygon | required | All Polygon, none Multi, so an explode step cannot inflate the row count. None empty. 2,036 (1.4%) carry a ring self-intersection, every one repaired by a zero-width buffer |

Areas run from 8 m² to 1,927 ha, median 2,911 m², mean 14,026 m², totalling 207,231 ha. The spread
is wide — p25 is 723 m², p75 0.95 ha — because alpine pastures share the layer with vegetable plots.
295 features (0.2%) are 10 m² or smaller.

The 100 `CODE` values group by prefix:

| Prefix | Codes | Rows | Share | Area (ha) | Meaning |
| --- | --: | --: | --: | --: | --- |
| `AP` | 7 | 43,439 | 29.4% | 57,349 | Meadow (`AP2` Prato stabile alone is 41,145 rows) |
| `AL` | 7 | 37,732 | 25.5% | 111,433 | Alpine pasture, graded by tree cover, rock cover or *tara* percentage |
| `FR` | 18 | 23,204 | 15.7% | 17,964 | Fruit (`FR1` Mela is 19,016 rows) |
| `PA` | 4 | 12,274 | 8.3% | 6,523 | Pasture |
| `AS` | 6 | 9,399 | 6.4% | 3,176 | Special-purpose meadow |
| `AV` | 1 | 7,240 | 4.9% | 5,838 | Viticulture |
| `AA` | 39 | 6,309 | 4.3% | 1,109 | Arable and field vegetables — the long tail of the list |
| `SI` | 1 | 3,471 | 2.3% | 142 | Hedges |
| `AF` | 5 | 2,902 | 2.0% | 3,132 | Fodder |
| `CA`, `SE`, `VI`, `AW`, `ANA`, `FO` | 12 | 1,573 | 1.1% | 566 | Chestnut grove, greenhouse, nursery, vineyard set-aside, other, forest |

`SI` (hedges) and `FO` (forest, 32 rows) are landscape rather than crop classes.

### Example

Count the features, then request one page:

    …/ows?service=WFS&version=2.0.0&request=GetFeature&typeNames=p_bz-Agriculture:Fields-Used&resultType=hits
    …/ows?service=WFS&version=2.0.0&request=GetFeature&typeNames=p_bz-Agriculture:Fields-Used&count=1000&startIndex=0&outputFormat=application/json

One feature, retrieved with `cql_filter=ID=278846`, with the coordinate list and the null
properties truncated:

```json
{
  "type": "Feature",
  "id": "Fields-Used.278846",
  "geometry": { "type": "Polygon", "coordinates": [[[624352.7, 5165183.7], [624406.5, 5165308.5], …]] },
  "properties": {
    "ID": 278846,
    "CODE": "AA13",
    "DESCRIPTION_IT": "Patata da consumo",
    "DESCRIPTION_DE": "Speisekartoffeln",
    "BEGIN_DATE": "2025-07-28Z",
    "END_DATE": "9999-12-31Z",
    "LAST_MODIFY": "2025-09-03Z",
    "USER": "--AF_ETL_IMPORT--",
    "AREA": 4152
  }
}
```

## API

| Standard | URL |
| --- | --- |
| OGC WFS 2.0.0 | https://geoservices6.civis.bz.it/geoserver/p_bz-Agriculture/ows?service=WFS&version=2.0.0&request=GetCapabilities |
| OGC WMS 1.3.0 | https://geoservices6.civis.bz.it/geoserver/p_bz-Agriculture/ows?service=WMS&version=1.3.0&request=GetCapabilities |
| Catalogue record | https://data.civis.bz.it/dataset/superficie-agricola-utilizzata |

The service is GeoServer. A response is capped at 110,000 features, so the whole layer takes two
pages, and `startIndex` paging is stable without an explicit sort — a full pass returns exactly
147,743 distinct `ID` values. `resultType=hits` reports the true count. `propertyName` and
`cql_filter` are both supported.
