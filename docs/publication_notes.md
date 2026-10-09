# Publication and reproducibility notes

Target journal: **Journal of Equine Veterinary Science (JEVS)**, Elsevier, ISSN 0737-0806. This repository contains supporting data and analysis code; no manuscript was supplied.

The proposed folders separate source measurements, annotations, analysis, and generated artifacts. JEVS does not prescribe this particular GitHub layout. Consult the official [Guide for Authors](https://www.sciencedirect.com/journal/journal-of-equine-veterinary-science/publish/guide-for-authors) before submission. Its contents could not be retrieved during preparation (HTTP 403), so this layout is not a certification of journal compliance.

## Notebook adaptation

`weight_estimation_keypoints.ipynb` is the unchanged original. `notebooks/weight_estimation_keypoints_jevs.ipynb` is a separate working copy with repository-relative paths, output folders, cleared execution state, and an explicit warning about missing prerequisites. The original modeling workflow and exploratory analyses are retained; no new scientific results are claimed.

Before using results in the paper:

- Resolve the physical measurement units and record the calibration method.
- Provide image-to-row mapping for perspective analyses and the missing `neck_posture` labels if those analyses are retained.
- Review sections requiring `BCS`, `Geburtsjahr`, `Rasse`, `Stockmaß`, `Körperlänge`, `Brustumfang`, and `image_name`; these are absent from the measurement CSVs. Missing optional columns are tolerated in export/preprocessing drops in the copy, but analyses requiring them still need revision.
- Supply original images and `keypoints3.json` for the image visualization, or omit that section from the released analysis.
- Review feature selection and tuning: the original correlation ranking uses the full dataset, some feature rankings are computed before cross-validation, and the same CV folds are used for tuning and reporting. These exploratory estimates should not be presented as unbiased validation; fit selection inside training folds and reserve the horse-grouped test set for final evaluation.
- Execute the notebook in a clean environment, resolve remaining exploratory variable dependencies, verify metrics and exports, then record exact dependency versions.

## Preparing a citable release

Add the final paper title, author list, publication reference, repository URL, and archived release DOI when known. Match the manuscript's data/code availability statement to the files actually released. A possible draft, to finalize only after publication of the repository, is:

> The measurement datasets and analysis code are available at [repository URL], archived as [version/release DOI]. Code is provided under the MIT License and datasets under CC BY-NC 4.0. [Describe any unavailable source images or annotations and the applicable access conditions.]

Keep figure legends, units, table descriptions, supplementary-file numbering, ethical approval/consent information, and author declarations consistent with the manuscript. Author-specific statements cannot be inferred from these files.
