# Estimating Equine Body Weight from Single Images Using Extended Keypoints

Research data and analysis code supporting a paper intended for the **Journal of Equine Veterinary Science (JEVS)**.

## Repository structure

```text
horse-bm-weight/
├── README.md
├── LICENSE-CODE                   # MIT license for code
├── LICENSE-DATA                   # CC BY-NC 4.0 license for data
├── requirements.txt               # Notebook dependencies
├── data/
│   ├── weights_bm_pixel.csv
│   ├── weights_bm_meter.csv
│   ├── labels_perspective.csv
│   └── data_dictionary.md         # Explanaition of the data
└── notebooks/
    └── weight_estimation_keypoints_jevs_copy.ipynb
```

## Data and reuse

See the [data dictionary](data/data_dictionary.md) for file formats, observed dataset dimensions, and metadata.

Code is licensed under [MIT](LICENSE-CODE). Research data in `data/` are licensed under [CC BY-NC 4.0](LICENSE-DATA).

## Abstract

Body weight in horses is a relevant factor for many aspects of horse care, feeding, and medication. Common measurement methods, such as using a scale or measuring the horse with measuring tapes, require high personnel and financial costs and can cause stress to the animals.
This study presents a non-invasive approach to weighing horses. The aim is to extract body measurements from a single image of a horse using keypoints and to generate a precise weight estimate using machine learning methods. Additionally, the study analyzes how the image’s perspective and the horse’s head position influence the calculation.
Common algorithms such as Random Forest, XGBoost, and multiple linear regression are used.
All methods produce an average error of 29.7 to 34.9 kg, although there are significant differences among the various horse types. Furthermore, all models are able to base their calculations on body measurements that are only slightly influenced by perspective and head position.
These initial tests demonstrate a promising method for performing non-invasive weight estimation in horses.
