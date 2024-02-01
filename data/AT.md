# Austria: INVEKOS Referenzen Österreich 2021

## Submission Details

- **Submitter (Affiliation):** Matthias Mohr
- **Data Provider (Legal Entity):** Agrarmarkt Austria (Government)
- **Homepage:** https://geometadatensuche.inspire.gv.at/metadatensuche/inspire/api/records/9db8a0c3-e92a-4df4-9d55-8210e326a7ed

## Overview

The layer includes all reference parcels ("Referenzparzellen") defined by the paying agency Agrarmarkt Austria and recorded landscape elements (landscape element layers) within the meaning of Art. 5 of Regulation (EU) No. 640/2014 and Regulation of the competent federal ministry with horizontal rules for the area of the Common Agricultural Policy (Horizontal CAP Regulation) StF: Federal Law Gazette II No. 100/2015.

Reference parcel: is the physical block that can be clearly delimited from the outside (e.g. forest, roads, water bodies) and is formed by contiguous agricultural areas that are recognizable in nature.

## Data & Metadata

- **URL:**
  - GeoPackage: https://inspire.lfrz.gv.at/009501/ds/inspire_referenzen_2021_polygon.gpkg.zip
  - GML: https://inspire.lfrz.gv.at/009501/ds/inspire_referenzen_2021_polygon.gml.zip
- **Documentation:** https://www.data.gv.at/katalog/dataset/ama_invekosreferenzensterreich2021/resource/2359389c-15c2-4ba0-ba03-d57f3d109460
  Documentation about the metadata is missing, thus the descriptions and constraints below are partially assumptions and partially missing.
- **File Format:** GeoPackage / GML
- **Geometry Format (if different from data):** - (Points available in addition to Polygons)
- **Metadata Format (if different from data):** INSPIRE (ISO 19115)
- **Projection:** EPSG:31287
- **License:** CC-BY-4.0

### Properties

| Property            | Data Type | Constraints | Description                                                  |
| ------------------- | --------- | ----------- | ------------------------------------------------------------ |
| fid                 | integer   |             | Identifier. Example: `201`                                   |
| RFL_ID              | number    |             | Identifier. Example: `107439377`                             |
| REF_ART             | string    |             | Type of field. One of: `ALM`,  `HEIM`, `HW`, `LSE_FL`, `PF`  |
| BRUTTOFLAECHE_HA    | number    |             | Gross area in ha. Example: `6,485508`                        |
| INSPIRE_ID          | string    |             | INSPIRE Identifier. Example: `https://data.inspire.gv.at/0095/9db8a0c3-e92a-4df4-9d55-8210e326a7ed/elu.ExistingLandUseObject/108601900154/MFA-2021` |
| GML_ID              | string    |             | GML Identifier. Example: `AT.0095.9db8a0c3-e92a-4df4-9d55-8210e326a7ed.elu.ExistingLandUseObject.108601900154.MFA-2021` |
| GML_IDENTIFIER      | string    |             | GML Identifier. Example: `https://data.inspire.gv.at/0095/9db8a0c3-e92a-4df4-9d55-8210e326a7ed/elu.ExistingLandUseObject/108601900154/MFA-2021` |
| REF_ART_BEZEICHNUNG | string    |             | Type of field in a more human-readable version of `REF_ART`. One of: `Alm`, `Heimgut`, `Hutweide`, `LSE Fläche`, `Pflegefläche` |
| REFERENZ_KENNUNG    | number    |             | Example: `108601900154`                                      |
| FART_ID             | number    |             | Example: `1696`                                              |
| GEO_TYPE            | string    |             | Example: `POLYGON`                                           |
| GEO_DATAREF         | string    | date-time   | Example: `2017-01-23 22:16:00`                               |
| GML_GEOM            | binary    |             | GML Geometry (see below)                                     |
| GML_LENGTH          | number    |             | Number of bytes of the GML_GEOM field. Example: `10719`      |

Mapping of `REF_ART` and `REF_ART_BEZEICHNUNG`:

- `ALM` = `Alm`
- `HEIM` = `Heimgut`
- `HW` = `Hutweide`
- `LSE_FL` = `LSE Fläche`
- `PF` = `Pflegefläche`

Example for `GML_GEOM`:
```xml
<gml:Polygon gml:id="ID0001" srsName="EPSG:3035" xmlns:gml="http://www.opengis.net/gml/3.2">
	<gml:exterior>
		<gml:LinearRing>
			<gml:posList srsDimension="2">4354889.29482811 [...] 2716301.28531537 </gml:posList>
		</gml:LinearRing>
	</gml:exterior>
	<gml:interior>
		<gml:LinearRing>
			<gml:posList srsDimension="2">4355360.7216415 [...] 2716403.23876317 </gml:posList>
		</gml:LinearRing>
	</gml:interior>
</gml:Polygon>
```

## API

No publicly documented API found.