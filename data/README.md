# Dataset Setup

GeoVision AI uses the **images_dataSAT** satellite-image dataset for binary image classification:

- `class_0_non_agri` — non-agricultural land (label `0`)
- `class_1_agri` — agricultural land (label `1`)

## Download

Download the archive from the source used by the original course notebooks:

<https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/4Z1fwRR295-1O3PMQBH6Dg/images-dataSAT.tar>

Dataset access was confirmed by the project maintainer. The archive has not been independently inventoried as part of this project, so image counts, native dimensions, file formats, and integrity are not asserted here.


## Local placement

Keep the dataset outside Git-tracked source code. Place the downloaded archive at:


```text
data/raw/images-dataSAT.tar
```

Extract it locally so the dataset directory is available in this expected layout:


```text
data/
└── raw/
    └── images_dataSAT/
        ├── class_0_non_agri/
        └── class_1_agri/
```

If the archive extracts to a different nesting level, adjust the local placement so the two class directories are directly under `images_dataSAT/`.

## Dataset handling notes

- Do not commit the archive or extracted images to Git.
- Dataset licensing, redistribution rights, and commercial-use permission have not been verified. Treat the dataset as externally sourced and do not redistribute it.
- The model pipeline may resize images to `64 × 64` and convert them to RGB, matching preprocessing used in the original notebooks. This is preprocessing behavior, not a verified statement about the images' native dimensions or channels.
- Dataset inventory and image-integrity checks are currently skipped by explicit project decision. They may be revisited if issues arise during pipeline development.

## Class mapping

| Directory | Label | Meaning |
|---|---:|---|
| `class_0_non_agri` | 0 | Non-agricultural land |
| `class_1_agri` | 1 | Agricultural land |