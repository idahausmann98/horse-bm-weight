# Equine body weight estimation from image-derived body measurements

Research data and analysis code supporting a paper intended for the **Journal of Equine Veterinary Science (JEVS)**.

## Repository structure

```text
horse-bm-weight/
├── README.md
├── LICENSE-CODE                   # MIT license for code
├── LICENSE-DATA                   # CC BY-NC 4.0 license for data
├── requirements.txt               # Notebook dependencies
├── weight_estimation_keypoints.ipynb # Unmodified original notebook
├── data/
│   ├── raw/
│   │   ├── weights_bm_pixel.csv
│   │   └── weights_bm_meter.csv
│   └── annotations/
│       └── labels_perspective.csv
├── notebooks/
│   └── weight_estimation_keypoints_jevs.ipynb # Working copy
├── docs/
│   ├── data_dictionary.md
│   └── publication_notes.md
└── results/
    ├── figures/
    ├── tables/
    ├── models/
    └── parameters/
```

This is a proposed research-repository layout, not a journal-mandated folder structure. Input CSV files retain their original contents and names. The original notebook remains at its original location.

## Working with the notebook

Create a Python environment, then run:

```sh
python -m pip install -r requirements.txt
jupyter lab notebooks/weight_estimation_keypoints_jevs.ipynb
```

The working copy resolves paths from the repository root or the `notebooks/` directory. It reads pixel measurements by default; the alternative dataset can be selected in the configuration cell. Generated files are directed to `results/`, and historical notebook outputs have been cleared.

**Execution status:** the working copy is an adapted exploratory analysis, not yet a validated, end-to-end reproduction of the paper. Some original analyses require columns, posture labels, images, and keypoint annotations that are not present in the supplied files. See [publication notes](docs/publication_notes.md) before running these sections. Dependency versions are not locked because no validated Python environment was supplied.

## Data and reuse

See the [data dictionary](docs/data_dictionary.md) for file formats, observed dataset dimensions, and unresolved metadata. Source data must not be overwritten with generated exports.

Code is licensed under [MIT](LICENSE-CODE). Research data in `data/` are licensed under [CC BY-NC 4.0](LICENSE-DATA). Publication metadata, a public repository URL, and an archived release DOI should be added when available.

The journal's [Guide for Authors](https://www.sciencedirect.com/journal/journal-of-equine-veterinary-science/publish/guide-for-authors) is the authoritative source for submission requirements.
