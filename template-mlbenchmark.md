# Title <!-- Replace with your title of the dataset -->

## Submission Details

- **Submitter (Affiliation):** John Doe, Example Corp.
- **Data Provider (Legal Entity):** Field Data, Inc. (Company/Government/Individual/Other)
- **Homepage:** https://homepage.example/data

## Overview

<!-- Please provide a short overview about your data and/or API. -->

## Data

<!-- Any important information about your ML benchmark field boundary dataset and metadata,
e.g. what satellite datasets were used. -->

- **URL:** https://data.example/files/ (does not need to be the whole dataset, can just be a couple rows of representative data)
- **Documentation:** https://docs.data.example
- **File Format:** GeoTIFF, JPEG, Numpy arrays, etc.
- **Geographic Coverage:** India, Ghana, etc.
- **Has Train/Test split?:** Yes/No
- **Input data sensor(s):** Sentinel-2, Sentinel-1, PlanetScope, etc.
- **Input patch size:** e.g., 256x256 pixels
- **Input data channels(s):** RGB, NIR, VV/VH, etc. Include number of channels.
- **Input data timesteps:** 1, 12 (monthly), 2 (seasonally), etc.
- **Label information:**
  - [ ] Semantic segmentation (binary masks)
  - [ ] Instance segmentation (instance masks)
  - [ ] Panoptic segmentation (complete-image instance masks)
  - [ ] Includes crop type or category labels
  - [ ] Ground truth polygons (vector data used to create label masks)
- **Projection (if georeferenced):** EPSG:4326/...
- **License:** CC-0/Commercial/...
- **Data Creation Details:** Publication or other source of information about how dataset was constructed
- **Label Source:** Dataset of original ground truth labels used to create this dataset (may be a link to the dataset file in this repo)
  
...

### Metadata
<!-- Describe any metadata provided with the samples, if available. -->

### Dataset splits
<!-- Include details about the dataset splits, if available. -->

**Type of split:** e.g., uniform at random, geographically-partitioned, etc.

| Subset | # samples |
| ----- | -------- |
| Total | integer |
| Train | integer |
| Validation | integer |
| Test | integer |

### SOTA performance

<!-- If the dataset was published with state-of-the-art (SOTA) performance for benchmarking, include those metrics here. -->

| Model | OA | F1 | IoU | mAP |
| ----- | -- | -- | --- | --- |
| name | 0-100 | 0-100 | 0-100 | 0-100 |

### Example

<!-- Please provide a representative image to visualize the data, if available. -->

## API (optional)

<!-- If the dataset provides an API, python package, or other software for loading the dataset, 
include details about it here. -->

| Library/package | URL |
| -------- | --- |
| Library name | https://data.example/api/ |

### Example

<!-- Please provide a link to the data or embed it into this document as a code block. -->
