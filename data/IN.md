# India
## Submission Details

- **Submitter (Affiliation):** Snehal Chaudhari, ASU.
- **Data Provider (Legal Entity):** Sherrie Wang, Francois Waldner, David B. Lobell
- **Homepage:** https://www.mdpi.com/2072-4292/14/22/5738

## Overview
The data containing 10,000 crop field boundaries in India and weights of the best-performing model. This dataset accompanies the paper "Unlocking large-scale crop field delineation in smallholder farming systems with transfer learning and weak supervision" (forthcoming in Remote Sensing). Ten thousand crop fields in India were delineated manually through inspection of high-resolution satellite imagery (Airbus SPOT).The weights of the highest performing neural network (FracTAL ResUNet architecture) pre-trained in France and fine-tuned on Airbus SPOT images in India are also provided. The model was trained in MXNet 1.6.0 and can be loaded with the "model.load_parameters()" function.

## Data

<!-- Any important information about your field boundary data and metadata,
e.g. in which format and projection the geometry is provided. -->

- **URL:** https://zenodo.org/records/7315090
- **Documentation:**  https://www.mdpi.com/2072-4292/14/22/5738
- **File Format:** Shapefile
- **Geometry Format (if different from data):** -
- **Metadata Format (if different from data):** -
- **Projection:** WGS 84
- **License:** CC BY 4.0
- **Computer Vision / AI Details:** At first, human workers labeled 5 fields per image across 2000 images from throughout India. By training models on partial labels instead of fully-segmented labels, the authors reduced the labeling burden, sampled a broader diversity of landscapes across India, and decoupled field delineation from cropland mapping. Second, a neural network was pre-trained on partial field boundary data in France, where a large dataset of government-collected field boundaries is available. Lastly, the model was fine-tuned to predict partial field boundaries in India using either PlanetScope or Airbus SPOT imagery. 


### Properties

<!-- A list of properties with e.g. a short description, data type, constraints such as value range or allowed values, etc. This can be found by opening the data file in qgis, then 
   right clicking on the layer and selecting 'layer properties', and then going to the 'fields' section. The 'name' in qgis is the property in this table, and the 'Type name' is the Data Type -->

| Property | Data Type | Constraints | Description       |
| -------- | --------- | ----------- | ----------------- |
| sample   | integer   | 0-2002      | Sample image ID   |

### Example

| Property   | Example Value    |
| ---------- | ---------------- |
| sample     | 2002             |

## API (optional)

No publicly documented API found.

