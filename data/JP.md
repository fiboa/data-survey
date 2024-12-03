# Japan Crop Fields (Fude)

## Submission Details

- **Conversion and Compilation:** Hiroo Imaki, Pacific Spatial Solutions
- **Submitter (Affiliation):** Ivor Bosloper
- **Data Provider (Legal Entity):** Japanese Ministry of Agriculture, Forestry and Fisheries (MAFF, 農林水産省)
- **Homepage:** https://www.maff.go.jp/

## Overview

This submission is based on analysis and compilation of Hiroo Imaki as described 
[in a LinkedIn Post](https://www.linkedin.com/posts/hiroo-imaki-b656963b_sourcecooperative-activity-7266885356606676992--RRS).

Japanese Farmland Parcel Polygons (Fude Polygons in Japanese) represent parcel information of farmland. 
The polygons are manually digitized data derived from aerial imagery, such as satellite images. Since no 
on-site verification or similar procedures have been conducted, the data may not necessarily match the actual 
current conditions. Fude Polygons are created for the purpose of roughly indicating the locations of farmland.

The data is originally published on by [the Japanese Ministry of Agriculture](https://www.maff.go.jp/j/tokei/porigon/). 
As it is described and documented in Japanese, requires a specific Japanse gBizID account, the data is a bit hard to 
find. This submission is based on the compiled & converted data.

## Data & Metadata

- **URL:** https://source.coop/repositories/pacificspatial/field-polygon-jp/description
- **Documentation:** https://www.maff.go.jp/j/tokei/porigon/ (Japanese)
- **File Format:** GeoParquet
- **Projection:** 
- **License:** CC-BY
- **Attribution:** Fude Polygon Data (published for the fiscal years 2021, 2022, 2023, and 2024) provided by the Ministry of Agriculture, Forestry and Fisheries, processed by Pacific Spatial Solutions, Inc

The boundaries of crop fields supposed to fit within the reference parcels. The used crop classification
is a mix of pure crops, crop categories, land cover types and attributes used for specific subsidy requirements.
Currently, the publishing organization doesn't mention _crop_ but designates this attribute as _land cover_.

### Properties

|------------------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| polygon_uuid           |  string   | Fude Polygon ID (UUID ver. 4)                                                                                                                                                                           | 筆ポリゴンID（UUID ver. 4）                                                                                    |
| land_type              |  string   | Land use code (rice field or field) determined by visual interpretation of satellite imagery                                                                                                            | 衛星画像の目視判読による田、畑の地目コード                                                                     |
| issue_year             |  string   | Year of publication on the site                                                                                                                                                                         | サイトに公開した年度                                                                                           |
| edit_year              |  string   | Year of creation or update                                                                                                                                                                              | 新規作成、更新した年度                                                                                         |
| history_ja             |  string   | Information indicating the relationship with previously published field polygons (in JSON format)                                                                                                       | 過去に公開した筆ポリゴンとの関係を示した情報（JSON形式）                                                       |
| history_en             |  string   | English translation of the attribute values in history_ja                                                                                                                                               | history_jaの属性値の英語訳                                                                                     |
| last_polygon_uuid      |  string   | If the data is the same as the previous year,  the polygon_id of the previous year. If there are changes,  it is set to NULL.                                                                           | 前年度のデータと同一の場合は前年度のpolygon_id。変更があった場合はNULL                                         |
| prev_last_polygon_uuid |  string   | If the data is the same as both the previous year and the year before,  the polygon_id of the previous year. If changes occurred between the year before last and the current year,  it is set to NULL. | 前年度、前々年度のデータと同一の場合は前年度のpolygon_id。前々年度から当該年度までの間に変更があった場合はNULL |
| local_government_cd    |  string   | Code of the municipality,  as defined by the Ministry of Internal Affairs and Communications,  where the centroid of the polygon overlaps.                                                              | ポリゴンの重心点と重なる市区町村の総務省地方公共団体コード                                                     |
| point_lng              |  string   | Longitude of the polygon’s centroid                                                                                                                                                                     | ポリゴン重心点の経度                                                                                           |
| point_lat              |  string   | Latitude of the polygon’s centroid                                                                                                                                                                      | ポリゴンの重心点の緯度                                                                                         |
| old_polygon_id         |  string   | polygon_id of the data published in 2021                                                                                                                                                                | 2021年公開データのpolygon_id                                                                                   |
| land_type_ja           |  string   | Japanese notation for land_type code (田 for rice field,  畑 for field)                                                                                                                                 | land_typeコードの日本語表記（田、または畑）                                                                    |
| land_type_en           |  string   | English notation for land_type code (rice_field for rice field, field for field),                                                                                                                      | land_typeコードの英語表記（rice_field または field）                                                           |


### English Translations for the Attribute Values
| Japanese  | English          |
|-----------|------------------|
| 筆ポリゴン     | field_polygon_id |
| 更新年度      | fy_updated       |
| 前年同一      | same_prev_fy     |
| 発生年度      | fy_occurence     |
| 関連        | related          |
| 発生        | appeared         |
| 消滅        | disappeared      |

### Example

See [example map](https://open.fude.maff.go.jp/)

## API

See https://www.fude.maff.go.jp/ . To use this service, you will need an eMAFF ID (gBizID).
