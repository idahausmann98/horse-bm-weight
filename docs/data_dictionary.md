# Data dictionary

## Supplied files

| File | Delimiter | Observed content |
| --- | --- | --- |
| `data/weights_bm_pixel.csv` | Comma | 199 rows, 82 horse IDs, 211 columns; body measurements in pixels |
| `data/weights_bm_meter.csv` | Comma | 199 rows, 82 horse IDs, 211 columns; body measurements in centimeter |
| `data/labels_perspective.csv` | Semicolon | Image filename, horse ID, and perspective label |

## Measurement columns

- `ID`: horse identifier; repeated IDs must stay in the same partition during model evaluation.
- `Typ`: horse-type category
- `Gewicht`: reference body weight in kilograms.
- Remaining 208 columns: Distances between two keypoints and the distance from each keypoint to the ground.


## Annotation columns

- `image_name`: image filename used to identify the annotation.
- `ID`: horse identifier; not a unique image identifier.
- `perspective`: code for the perspective (0 - good perspective, 1 - Forehand turned away, -1 - Hind legs turned away)

The measurement CSV files have no `image_name` column. Joining image-level labels using only `ID` could multiply rows or assign the wrong label to a measurement. A verified image-to-row mapping is needed. `neck_posture`, used in the original notebook, is not included in the annotation file.

Raw inputs are preserved unchanged. Any cleaning, unit conversion, or category mapping should be implemented in the working notebook and exported separately.
