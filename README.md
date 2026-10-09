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
