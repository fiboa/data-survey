# Saarland, Germany

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper; Saidy Barry, moreGeo GmbH (reference parcels)
- **Data Provider (Legal Entity):** Ministerium für Umwelt, Klima, Mobilität, Agrar und Verbraucherschutz, Saarland (Government)
- **Homepage:** https://geoportal.saarland.de

## Overview

Saarland publishes two complementary IACS / InVeKoS datasets, both transformed into INSPIRE data
models and served through the GDI-SL geoportal:

- **Application parcels ("Antragsschläge"):** the parcels declared by farmers for agricultural-land
  subsidies, published as INSPIRE *Existing Land Use* features.
- **Reference parcels ("LPIS-Referenzschläge"):** the reference parcels of the Land Parcel
  Identification System, published as INSPIRE *Land Cover* features. 62,304 parcels, each carrying
  a land cover class from the national IACS code list.

## Data

### Application parcels (Antragsschläge)

- **URL:** https://geoportal.saarland.de/gdi-sl/inspirewfs_Existierende_Bodennutzung_Antragsschlaege
- **Documentation:** https://geoportal.saarland.de
- **File Format:** GML 3.2 (INSPIRE *Existing Land Use*)
- **Projection:** EPSG:4258 (ETRS89)
- **License:** CC-BY-4.0
- **Attribution:** ©GDI-SL 2024

#### Properties

| Property                                      | Data Type    | Constraints      | Description                                                                   |
| --------------------------------------------- | ------------ | ---------------- | ----------------------------------------------------------------------------- |
| `gml:identifier`                              | string       | required, unique | INSPIRE identifier, e.g. `…/ExistingLandUseObject_ed03310d…_DESLLI00002529002224568`; the FLIK is embedded in its last segment |
| `elu:inspireId` → `localId` / `namespace`     | string       | required         | The same identifier split into its two INSPIRE parts                          |
| `gml:name`                                    | string       | required         | Crop group as a German label, e.g. `Dauergrünland` (16 values)                 |
| `elu:specificLandUse`                         | xlink        | required         | The same crop group as an `xlink:href` into [`de.iacs/CropValue`](https://registry.gdi-de.org/codelist/de.iacs/CropValue) |
| `elu:hilucsLandUse`                           | xlink        | required         | HILUCS land use; always `1_1_Agriculture`                                      |
| `elu:beginLifespanVersion` / `elu:observationDate` | date-time | always `xsi:nil` | The only date fields; never populated                                          |
| `elu:hilucsPresence` / `elu:specificPresence` | —            | always `xsi:nil` | INSPIRE presence attributes; never populated                                   |
| `elu:geometry`                                | MultiSurface | required         | Parcel geometry, always a single `gml:surfaceMember`                           |

54,038 parcels (counted 2026-09-11). Unlike the reference-parcel service, this one serves **no
`gml:description`**, so neither the FLIK nor the parcel area is available as a value: the FLIK is
the first 16 characters of the identifier's last underscore-separated segment
(`…_DESLLI00002529002224568` → `DESLLI0000252900`, the remaining seven digits numbering the parcel
within the field block), and the area has to be computed from the geometry. With every date field
nil, the data carries no vintage of its own; the GDI-DE dataset record
`9fc76dc8-da6d-4e70-a2fa-b930843174b8` declares `revisionDate` 2026-01-01.

#### Example

Count the features, then request one page:

    …/inspirewfs_Existierende_Bodennutzung_Antragsschlaege?SERVICE=WFS&VERSION=2.0.0&REQUEST=GetFeature&typeNames=elu:ExistingLandUseObject&resultType=hits
    …/inspirewfs_Existierende_Bodennutzung_Antragsschlaege?SERVICE=WFS&VERSION=2.0.0&REQUEST=GetFeature&typeNames=elu:ExistingLandUseObject&outputFormat=application/gml%2Bxml;%20version=3.2&count=2500&startIndex=0

### Reference parcels (LPIS-Referenzschläge)

- **URL:** https://geoportal.saarland.de/gdi-sl/inspirewfs_Bodenbedeckung_LPIS
- **Documentation:** https://geoportal.saarland.de/spatial-objects/384
- **File Format:** GML 3.2 (INSPIRE *Land Cover* 5.0); GeoJSON via the OGC API - Features endpoint
- **Projection:** EPSG:4258 (ETRS89), declared per geometry as `urn:ogc:def:crs:EPSG::4258`
- **License:** [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/deed.de), stated in the
  dataset metadata record as *"Lizenz: cc-by/4.0 … Quellenvermerk: © GDI-SL (Jahr)"*
- **Attribution:** © GDI-SL 2026, CC BY 4.0

62,304 reference parcels. The FLIK identifier and the parcel size are encoded inside the INSPIRE
`description` attribute rather than in dedicated fields. The land cover class is carried as an
`xlink:href` into the national IACS code list
[`de.iacs/AgriculturalAreaTypeValue`](https://registry.gdi-de.org/codelist/de.iacs/AgriculturalAreaTypeValue),
the same code list Bavaria and Hesse publish:

- `GL` — Dauergrünland (permanent grassland), 61.4%
- `AL` — Ackerland (arable land), 36.6%
- `DK` — Dauerkultur (permanent crop), 1.7%
- `S` — Sonstiges (other), 0.3%

Shares are from 5,000 parcels sampled across five offsets. Note that the class is present **only in
the GML**; the GeoJSON representation of the OGC API endpoint omits the nested
`landCoverObservation` and therefore carries no class at all.

#### Properties

| Property                                          | Data Type | Constraints        | Description                                                                   |
| ------------------------------------------------- | --------- | ------------------ | ----------------------------------------------------------------------------- |
| `gml:description`                                 | string    | required           | Encodes the parcel size and the FLIK, e.g. `Size in ha: 0.11206, flik: DESLLI0000248744` |
| `gml:identifier`                                  | string    | required, unique   | INSPIRE identifier, e.g. `https://registry.gdi-de.org/id/de.sl.inspire.lc.ivs.lpis_sl/LandCoverUnit_…_DESLLI0100223113` |
| `lcv:inspireId` → `localId` / `namespace`         | string    | required           | The same identifier split into its two INSPIRE parts                          |
| `lcv:class`                                       | xlink     | required           | Land cover class, as an `xlink:href` into the `de.iacs` code list (values above) |
| `lcv:beginLifespanVersion`                        | date-time | always `xsi:nil`   | Date the record version was created; never populated                          |
| `lcv:mosaic` / `lcv:observationDate`              | —         | always `xsi:nil`   | INSPIRE Land Cover attributes; never populated                                |
| `lcv:geometry`                                    | Polygon   | required           | Parcel geometry                                                               |

The FLIK is 16 characters, `DESLLI` plus 10 digits, and unique. Parcel sizes range from 1.1 m² to
about 14 ha; small values are written in **scientific notation**, e.g. `Size in ha: 1.0999999999999999E-4`.

#### Example

Count the features, then request one page:

    …/inspirewfs_Bodenbedeckung_LPIS?SERVICE=WFS&VERSION=2.0.0&REQUEST=GetFeature&typeNames=lcv:LandCoverUnit&resultType=hits
    …/inspirewfs_Bodenbedeckung_LPIS?SERVICE=WFS&VERSION=2.0.0&REQUEST=GetFeature&typeNames=lcv:LandCoverUnit&count=2500&startIndex=0

One feature, with the coordinate list truncated:

```xml
<lcv:LandCoverUnit gml:id="LandCoverUnit_54030be6…_DESLLI0100223113">
  <gml:description>Size in ha: 1.0999999999999999E-4, flik: DESLLI0100223113</gml:description>
  <gml:identifier codeSpace="http://inspire.ec.europa.eu/ids">https://registry.gdi-de.org/id/de.sl.inspire.lc.ivs.lpis_sl/LandCoverUnit_54030be6…_DESLLI0100223113</gml:identifier>
  <lcv:geometry>
    <gml:Polygon srsName="urn:ogc:def:crs:EPSG::4258"><gml:exterior><gml:LinearRing>
      <gml:posList>49.186863 7.302103 …</gml:posList>
    </gml:LinearRing></gml:exterior></gml:Polygon>
  </lcv:geometry>
  <lcv:landCoverObservation>
    <lcv:LandCoverObservation>
      <lcv:class xlink:href="https://registry.gdi-de.org/codelist/de.iacs/AgriculturalAreaTypeValue/GL"/>
      <lcv:mosaic xsi:nil="true"/>
      <lcv:observationDate xsi:nil="true"/>
    </lcv:LandCoverObservation>
  </lcv:landCoverObservation>
</lcv:LandCoverUnit>
```

## API

| Standard           | URL                                                                                      | Documentation                                        |
| ------------------ | ---------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| OGC WFS 2.0.0      | https://geoportal.saarland.de/gdi-sl/inspirewfs_Existierende_Bodennutzung_Antragsschlaege | https://geoportal.saarland.de                        |
| OGC WFS 2.0.0      | https://geoportal.saarland.de/gdi-sl/inspirewfs_Bodenbedeckung_LPIS                      | https://geoportal.saarland.de/spatial-objects/384    |
| OGC API - Features | https://geoportal.saarland.de/spatial-objects/384/collections                            | https://geoportal.saarland.de/spatial-objects/384    |

Both WFS endpoints support `startIndex` / `count` paging and report `numberMatched` correctly, but
always report `numberReturned="0"`, so the page count has to be derived from a `resultType=hits`
request. The OGC API - Features endpoint accepts `limit` only from the fixed set
`1, 5, 10, 20, 50, 100, 200, 500, 1000, 2500`; any other value returns HTTP 200 with a plain-text
error rather than JSON. Both APIs return the parcels ordered by area, ascending.
