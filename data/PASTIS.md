# Panoptic Agricultural Satellite TIme-Series (PASTIS)

## Submission Details

- **Submitter (Affiliation):** Hannah Kerner
- **Data Provider (Legal Entity):** Vivien St Faire Garnot
- **Homepage:** https://github.com/VSainteuf/pastis-benchmark

## Overview

PASTIS is a benchmark dataset for panoptic and semantic segmentation of agricultural parcels from satellite time series. 
It contains 2,433 patches within the French metropolitan territory with panoptic annotations (instance index + semantic label for each pixel). 
Each patch is a Sentinel-2 multispectral image time series of variable length.

## Data

<!-- Any important information about your ML benchmark field boundary dataset and metadata,
e.g. what satellite datasets were used. -->

- **URL:** https://zenodo.org/record/5012942 
- **Documentation:** https://github.com/VSainteuf/pastis-benchmark/blob/main/documentation/pastis-documentation.pdf
- **File Format:** Numpy files
- **Geographic Coverage:** France (~4000 km2 sampled from four regions)
- **Has Train/Test split?:** Yes
- **Input data sensor(s):** Sentinel-2
- **Input patch size:** 128x128 pixels
- **Input data channels(s):** The 10 channels correspond to the non-atmospheric spectral bands of the Sentinel-2 satellite, after atmospheric correction and re-sampling at a spatial resolution of 10 meters per pixel.
- **Input data timesteps:** Variable length (30-60, all available Sentinel-2 acquisitions)
- **Label information:**
  - [ ] Semantic segmentation (binary masks)
  - [ ] Instance segmentation (instance masks)
  - [x] Panoptic segmentation (full-coverage instance masks)
  - [x] Includes crop type or category labels: 18 crop types plus a background class
  - [ ] Ground truth polygons (vector data used to create label masks)
- **Projection (if georeferenced):** N/A
- **License:** MIT License
- **Data Creation Details:** [Garnot et al., ICCV 2021](https://openaccess.thecvf.com/content/ICCV2021/papers/Garnot_Panoptic_Segmentation_of_Satellite_Image_Time_Series_With_Convolutional_Temporal_ICCV_2021_paper.pdf)
- **Label Source:** [France Graphical Plot Register (RPG)](https://www.data.gouv.fr/fr/datasets/registre-parcellaire-graphique-rpg-contours-des-parcelles-et-ilots-culturaux-et-leur-groupe-de-cultures-majoritaire/)

...

### Metadata
Splits used for 5-fold cross validation

### Dataset splits
Recommends using 5-fold cross validation rather than a single train/test split.

**Type of split:** 5-fold CV split uniform at random by patch

| Subset | # samples |
| ----- | -------- |
| Total | 2,433 |
| Train | n/a |
| Validation | n/a |
| Test | n/a |

### SOTA performance

<!-- If the dataset was published with state-of-the-art (SOTA) performance for benchmarking, include those metrics here. -->

| Model | OA | F1 | IoU | mAP |
| ----- | -- | -- | --- | --- |
| TSViT | 83.4%	|  | 65.4% | | |

### Example

![pastis](https://github.com/VSainteuf/pastis-benchmark/raw/main/images/predictions.png)

## API (optional)

<!-- If the dataset provides an API, python package, or other software for loading the dataset, 
include details about it here. -->

| Library/package | URL | 
| -------- | --- |
| Github repo | https://github.com/VSainteuf/pastis-benchmark |
| TorchGeo | https://torchgeo.readthedocs.io/en/stable/_modules/torchgeo/datasets/pastis.html | 

### Example

https://github.com/VSainteuf/pastis-benchmark/blob/main/demo.ipynb
