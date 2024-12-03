# Latvia Crop Fields (Lauku)

## Submission Details

- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Rural Support Service Republic of Latvia (Lauku atbalsta dienests)
- **Homepage:** https://www.lad.gov.lv/lv/lauku-registra-dati

## Overview

There's Field Blocks (Lauku bloku) and Fields (Lauki) for applications.

The land register is a geographic information system (GIS) that gathers information about agricultural land that is
eligible for state and European Union support from direct support scheme payments or environmental,
climate and rural landscape improvement payments.

The GIS of the field register contains a database of field blocks with interconnected spatial cartographic
data and information of attributes subordinate to them: geographic attachment, identification numbers
and area information.

## Data

- **URL:** https://karte.lad.gov.lv/arcgis/services/lauki/MapServer/WFSServer?request=GetFeature&service=wfs&version=2.0.0&typeNames=Lauki
- **Documentation:** https://www.lad.gov.lv/lv/lauku-registrs
- **Documentation:** https://www.lad.gov.lv/lv/lauku-registra-dati
- **File Format:** GML . Currently other GetCapabilities declared formats fail (like geopackage/shape)
- **Projection:** EPSG:3059
- **License:** WFS has no access constraints

### Properties

| Property            | Data Type | Constraints  | Description                      |
|---------------------|-----------|--------------|----------------------------------|
| PERIOD_CODE         | number    |              | year of application              |
| PARCEL_ID           | geometry  |              | identifier                       |
| PRODUCT_CODE        | number    |              | the code of the declared culture |
| PRODUCT_DESCRIPTION | string    |              | decoding of the cultural code    |
| AID_FORMS           | string    |              | types of support applied for     |
| AREA_DE CLARED      | float     |              | the claimed area                 |
| DATA_CHANGED_DATE   | date      |              | data change date                 |

## API (optional)

| Standard | URL | Documentation |
|----------| --- | ------------- |
| OGC WMS  | https://karte.lad.gov.lv/arcgis/services/lauku/MapServer/WMSServer | https://www.lad.gov.lv/lv/lauku-registra-dati |
| OGC WFS  | https://karte.lad.gov.lv/arcgis/services/lauki/MapServer/WFSServer | https://www.lad.gov.lv/lv/lauku-registra-dati |

### Example

https://karte.lad.gov.lv/arcgis/services/lauki/MapServer/WFSServer?request=GetFeature&service=wfs&version=2.0.0&typeNames=Lauki&count=1

```xml
<wfs:FeatureCollection xmlns:wfs="http://www.opengis.net/wfs/2.0"
                       xmlns:gml="http://www.opengis.net/gml/3.2"
                       xmlns:LAD="https://karte.lad.gov.lv/arcgis/services/lauki/MapServer/WFSServer"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                       timeStamp="2024-11-13T20:45:49Z" numberMatched="unknown" numberReturned="420694"
                       xsi:schemaLocation="http://www.opengis.net/wfs/2.0 http://schemas.opengis.net/wfs/2.0/wfs.xsd http://www.opengis.net/gml/3.2 http://schemas.opengis.net/gml/3.2.1/gml.xsd https://karte.lad.gov.lv/arcgis/services/lauki/MapServer/WFSServer https://karte.lad.gov.lv/arcgis/services/lauki/MapServer/WFSServer?service=wfs%26version=2.0.0%26request=DescribeFeatureType">
    <wfs:member>
        <LAD:Lauki gml:id="Lauki.4257003">
            <LAD:OBJECTID>4257003</LAD:OBJECTID>
            <LAD:PERIOD_CODE>2024</LAD:PERIOD_CODE>
            <LAD:PARCEL_ID>17420299</LAD:PARCEL_ID>
            <LAD:PRODUCT_CODE>111</LAD:PRODUCT_CODE>
            <LAD:AID_FORMS>MLS23</LAD:AID_FORMS>
            <LAD:AREA_DECLARED>1.02000000</LAD:AREA_DECLARED>
            <LAD:DATA_CHANGED_DATE>2024-10-09T07:19:59</LAD:DATA_CHANGED_DATE>
            <LAD:SHAPE>
                <gml:MultiSurface gml:id="Lauki.4257003.pl" srsName="urn:ogc:def:crs:EPSG::3059">
                    <gml:surfaceMember>
                        <gml:Polygon gml:id="Lauki.4257003.pl.0">
                            <gml:exterior>
                                <gml:LinearRing>
                                    <gml:posList>247528.97550000 674265.39470000 247528.45650000 674271.62300000
                                        247528.71090000 674271.74470000 247526.48540000 674277.86470000 247526.32960000
                                        674278.88840000 247516.01090000 674302.70100000 247515.41090000 674302.98670000
                                        247513.92770000 674307.86040000 247513.13390000 674310.24160000 247514.45680000
                                        674317.65000000 247516.30890000 674322.41250000 247517.89640000 674326.91040000
                                        247518.16100000 674333.78960000 247517.10270000 674343.57920000 247516.57350000
                                        674345.69590000 247455.98380000 674339.34590000 247452.01500000 674339.61040000
                                        247451.75050000 674340.93340000 247445.13590000 674367.92090000 247403.86080000
                                        674365.27510000 247403.69040000 674364.25300000 247403.26470000 674358.20690000
                                        247404.65450000 674341.99170000 247410.74000000 674300.98120000 247411.53370000
                                        674297.54160000 247413.91500000 674294.36660000 247417.09000000 674293.83740000
                                        247421.58790000 674292.51450000 247422.35960000 674291.51120000 247423.02600000
                                        674287.01320000 247423.60510000 674285.32850000 247425.04340000 674273.39590000
                                        247427.49190000 674256.86830000 247427.77480000 674255.54590000 247430.02640000
                                        674250.14190000 247430.05460000 674249.91650000 247430.11770000 674249.92280000
                                        247430.28570000 674249.51960000 247430.63080000 674249.97410000 247456.51300000
                                        674252.56230000 247470.27130000 674253.62070000 247483.85160000 674255.56070000
                                        247483.99620000 674255.34050000 247520.77340000 674261.16130000 247527.12340000
                                        674263.27800000 247528.97550000 674265.39470000
                                    </gml:posList>
                                </gml:LinearRing>
                            </gml:exterior>
                        </gml:Polygon>
                    </gml:surfaceMember>
                </gml:MultiSurface>
            </LAD:SHAPE>
            <LAD:PRODUCT_DESCRIPTION>Kvieši, vasaras</LAD:PRODUCT_DESCRIPTION>
            <LAD:SHAPE.AREA>10220.53563089</LAD:SHAPE.AREA>
            <LAD:SHAPE.LEN>445.60949431</LAD:SHAPE.LEN>
        </LAD:Lauki>
    </wfs:member>
</wfs:FeatureCollection>
```