# Lacuna Labels

A region-wide, multi-year set of crop field boundary labels for Africa

## Submission Details

- **Data Provider (Legal Entity):** Agricultural Impacts Research Group
- **Submitter (Affiliation):** Ivor Bosloper
- **Homepage:** https://github.com/agroimpacts/lacunalabels

## Overview

The [Lacunalabels](https://github.com/agroimpacts/lacunalabels/) repository hosts
the analytical code and pointers to datasets
resulting from a project to generate a continent-wide set of crop field
labels for Africa covering the years 2017-2023. The data are intended
for training and assessing machine learning models that can be used to
map agricultural fields over large areas and multiple years.

The project was funded by the [Lacuna Fund](https://lacunafund.org/),
and led by [Farmerline](https://farmerline.co/), in collaboration with
[Spatial Collective](https://spatialcollective.com/) and the
[Agricultural Impacts Research Group](agroimpacts.info) at [Clark
University](https://www.clarku.edu/departments/geography/).

Please refer to the [technical
report](docs/report/technical-report.pdf) for more details on the
methods used to develop the dataset, an analysis of label quality, and
usage guidelines.

Data is published at https://zenodo.org/records/11060871 and can be used in accordance
with 

## Data

- **URL:** https://zenodo.org/records/11060871
- **Documentation:** https://github.com/agroimpacts/lacunalabels
- **File Format:** geoparquet
- **Projection:** epsg:4326 (WGS 84)
- **License:** Planet’s [participant license agreement for the NICFI contract](https://go.planet.com/nicfi-pla-2024).

### Properties

| Property        | Data Type | Constraints | Description                                                               |
|-----------------|-----------|-------------|---------------------------------------------------------------------------|
| name            | String    |             | Identifier                                                                |
| assignment_id   | Number    |             | Identifier for each unique mapping assignment (1 mapping by 1 labeller)   |
| completion_time | DateTime  |             | Date and time the labelling assignment was completed                      |
| category        | String    |             | Course category; annualcropland, cloudshadow, fallow, treecrop, unsure1/2 |
