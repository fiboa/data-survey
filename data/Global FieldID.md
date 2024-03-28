# Global FieldID boundaries

## Submission Details

- **Submitter (Affiliation):** Andy Jenkinson, Varda AG
- **Data Provider (Legal Entity):** Varda AG
- **Homepage:** https://varda.ag/global-field-id

## Overview

The Global FieldID service provides a universal and spatiotemporally unique identifier for every field in the world, along with the multitude of boundaries associated with it. The service acts as a registry of the field and its spatial extent, providing access to IDs and boundaries via API, free web app and downloads. Data are aggregated from a combination of public open datasets, earth observation and ground truth data via 1st-party and 3rd-party channels.

## Data

The GFID data model includes objects representing:
* fields
* boundaries (polygons) stored in WGS84
* external cross-references and metadata
* temporal relationships between fields and boundaries
* spatial relationships between boundaries

GFID data is open by default, but permits registration of limited-access private data to enable discovery and/or private sharing networks. For every field, an openly accessible 'default' boundary must be provided; whilst users may contribute data to update the record, all default boundaries must be open.
- **Documentation:** [Developer Portal](https://developer.varda.ag/fid)
- **Downloads:** [Download Hub](https://fieldid.varda.ag/hub/downloads)
- **File Format:** GeoJSON
- **Projection:** EPSG:4326
- **License:** Mixed (see https://fieldid.varda.ag/terms-conditions)
- **Data Creation Details:** Combination of Official government, CV/AI output, Hand-drawn, machine-generated.
- **Computer Vision / AI Details:** Multiple third party sources (provenance metadata is retained)

...

### Properties

Properties of the `boundary` object, which is an object representing a cannonical boundary, deduplicated across multiple references from individual datasets. A boundary may or may not be the _defining_ boundary of a field object, and will have at least one 'boundary reference' indicating the original source(s) of this boundary geometry.

| Property             | Data Type      | Constraints        | Description |
| -------------------- | -------------- | ------------------ | ----------- |
| area                 | object (value and unit) | value is a double, unit is m2 | The area contained within the geometry. |
| representative_point | GeoJSON Position        | | A centroid position guaranteed to be inside the geometry. |
| centroid             | GeoJSON Position        | | The geometric centroid. |
| perimeter            | object (value and unit) | value is a double, unit is m | The exterior perimeter of the boundary. |
| country_iso_codes    | array (string) | ISO 3166-1 alpha-3 | The country(ies) the boundary falls within. Politically agnostic. |
| field_relationships  | array (object) | 0 to many | temporally-bound relationships with any field the boundary has been used to represent. |
| boundary_relationships | array (object) | 0 to many | quantified spatial overlap with any other boundaries. | 
| boundary_references | array (object) | 1 to many | Provenance metadata from the source(s) that have registered this boundary. | 

### Example

See API below

## API

| Standard | URL | Documentation |
| -------- | --- | ------------- |
| REST | https://api.varda.ag/fid/v1 | https://developer.varda.ag/fid |

### Examples

#### Field

```
{
    "field_id": "3TKQ.FMQB",
    "active_boundary_id": "028c67e7-a729-4d40-af08-3eafdc69e2de",
    "boundaries": [
        {
            "boundary_id": "028c67e7-a729-4d40-af08-3eafdc69e2de",
            "effective_from": "2023-07-03T20:08:13.237953+00:00",
            "effective_to": "9999-12-31T00:00:00+00:00"
        }
    ],
    "created_at": "2023-07-03T20:08:13.237953+00:00",
    "effective_from": "2023-07-03T20:08:13.237953+00:00",
    "effective_to": "9999-12-31T00:00:00+00:00"
}
```

#### Boundary
```
{
    "id": "028c67e7-a729-4d40-af08-3eafdc69e2de",
    "properties": {
        "area": {
            "unit": "m2",
            "value": 231167.896836
        },
        "boundary_references": [
            {
                "id": "8df503f6-a768-4d12-86a5-5262a2f43905",
                "varda:boundary_id": "028c67e7-a729-4d40-af08-3eafdc69e2de",
                "varda:delineation_type": "SATELLITE-GENERATED",
                "varda:source_name": "Digifarm 10m",
                "varda:user_provided_key": "9957",
                "varda:view_policy": []
            }
        ],
        "centroid": [ -53.303606492098, -18.71883101204598 ],
        "representative_point": [ -53.303625563674444, -18.718788077269696 ],
        "perimeter": {
            "unit": "m",
            "value": 2237.781283
        },
        "country_iso_codes": [ "BRA" ],
        "field_relationships": [
            {
                "effective_from": "2023-07-03T20:08:13.237953",
                "effective_to": "9999-12-31T00:00:00",
                "field_id": "3TKQ.FMQB",
                "type": "delineates"
            }
        ],
        "boundary_relationships": [
          {
            "type": "overlaps",
            "boundary_id": "123e4567-e89b-72d3-8456-426614174000",
            "intersection": 0.1,
            "intersection_area": 23116.8,
            "is_fixable_with_autoedit": true,
            "iou": 0.1
          }
        ]
    },
    "type": "Feature",
    "geometry": {
        "coordinates": [
            [
                [
                    [ -53.305758803901085, -18.714849112018133 ],
                    [ -53.30560760480204, -18.71476708388849 ],
                    [ -53.30268652981367, -18.71621371072573 ],
                    [ -53.301269306447914, -18.72282253856228 ],
                    [ -53.30469696940761, -18.721362443813664 ],
                    [ -53.305758803901085, -18.714849112018133 ]
                ]
            ]
        ],
        "type": "MultiPolygon"
    }
}
```
