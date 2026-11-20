# Dataset Provenance

## Dataset

**Name used in the source notebooks:** `images_dataSAT`  
**Purpose:** Binary satellite/geospatial image classification of agricultural versus non-agricultural land.

## Source

Primary source URL referenced by the Keras and PyTorch data-loading notebooks:

<https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/4Z1fwRR295-1O3PMQBH6Dg/images-dataSAT.tar>

The project maintainer confirmed that the archive can be downloaded.

A second URL was found in another original notebook:

<https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/5vTzHBmQUaRNJQe5szCyKw/images-dataSAT.tar>

This alternate source has not been verified to contain identical data and is not the primary source for this project.

## Access and licensing status

- Download access: confirmed by the project maintainer.
- License: not identified in the inspected notebook materials.
- Redistribution permission: unverified.
- Commercial-use permission: unverified.
- Attribution requirements: unverified.

**Policy:** Do not commit, mirror, bundle, or redistribute dataset files. Dataset access does not establish redistribution or commercial-use rights.


## Class labels

| Directory name | Numeric label | Class |
|---|---:|---|
| `class_0_non_agri` | 0 | Non-agricultural land |
| `class_1_agri` | 1 | Agricultural land |


## Directory layout expected by the notebooks

```text
images_dataSAT/
├── class_0_non_agri/
└── class_1_agri/
```

The PyTorch notebook's `ImageFolder` output confirms this class-to-index mapping.

## Image characteristics

The source notebooks use preprocessing that resizes images to **64 × 64** and converts them to RGB. This describes the notebook preprocessing target only; native image dimensions, channel layouts, formats, and image integrity have not been independently inventoried.

The notebooks report approximately 6,000 images and an 80/20 split (4,800 training and 1,200 validation) in one workflow. These figures are notebook-reported and have not been verified against the downloaded archive. Another notebook output shows 6,003 processed items; this is not treated as a confirmed image count.

## Verification status and scope decision

The project maintainer explicitly chose to skip the remaining dataset inventory checks during Step 1.3.

Not independently verified:
- total file/image count
- per-class counts and class balance
- native image dimensions
- native channels/color modes
- file-format distribution
- corrupt/unreadable files
- archive contents and exact nesting

These are documented as unknown rather than assumed.

## Dataset handling policy

- Keep dataset archives and extracted images local and untracked by Git.
- Do not claim redistribution or commercial-use rights without evidence.
- If data-loading or training issues indicate the skipped checks are necessary, revisit the inventory and licensing gate before proceeding further.

## Provenance record

| Field | Value |
|---|---|
| Primary source | Course-hosted S3 archive URL above |
| Access checked | Confirmed by project maintainer (date not recorded) |
| License | Unknown / not found in inspected notebook materials |
| Redistribution | Unverified; do not redistribute |
| Commercial use | Unverified |
| Attribution | Unknown |
| Dataset inventory | Skipped by explicit project decision |