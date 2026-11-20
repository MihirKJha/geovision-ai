# GeoVision AI

**Geospatial Computer Vision & Deep Learning**

GeoVision AI is an end-to-end computer vision project focused on geospatial image classification.

The initial use case is binary classification of satellite imagery into:

- Agricultural land
- Non-agricultural land

## Project Objectives

- Build reproducible computer vision data pipelines.
- Implement CNN-based image classifiers using PyTorch.
- Explore Vision Transformers (ViT).
- Experiment with CNN–ViT hybrid architectures.
- Evaluate deep learning models using appropriate classification metrics.
- Develop reusable components based on demonstrated reuse.
- Validate selected implementations using TensorFlow/Keras.
- Train and deploy a model using cloud infrastructure.

## Project Status

🚧 Initial project setup and data engineering.

## Technology Stack

- Python
- PyTorch
- Computer Vision
- CNN
- Vision Transformers
- TensorFlow/Keras (later phase)

## Scope

This project is developed incrementally, prioritizing correctness, reproducibility, maintainability and practical engineering over premature abstraction.

## Development Environment

GeoVision AI is developed using Python and an isolated virtual environment.

### Tested Environment

| Component | Version |
|---|---|
| Python | 3.x |
| PyTorch | x.x.x |
| torchvision | x.x.x |
| Pillow | x.x.x |
| PyYAML | x.x.x |
| pytest | x.x.x |
| Ruff | x.x.x |

### Development Tools

- pytest for automated testing
- Ruff for linting and formatting
- VS Code for development
- Virtual environment for dependency isolation


## VS Code Setup

### Prerequisites

- Python 3.11 or newer
- VS Code
- Python extension for VS Code

### Create the virtual environment

```powershell
python -m venv .venv
```

### Activate the environment

```powershell
.\.venv\Scripts\Activate.ps1
```

### Install the project

```powershell
python -m pip install -e ".[dev]"
```

### Select the Python interpreter

1. Open the project in VS Code.
2. Press `Ctrl + Shift + P`.
3. Select `Python: Select Interpreter`.
4. Choose the interpreter located at:

   `.venv\Scripts\python.exe`

### Verify the interpreter

```powershell
python -c "import sys; print(sys.executable)"
```

The interpreter should point to the project's `.venv` directory.


## Dataset

GeoVision AI uses the externally sourced `images_dataSAT` dataset for binary satellite-image classification:

- `class_0_non_agri` — non-agricultural land (label `0`)
- `class_1_agri` — agricultural land (label `1`)

Download the dataset from the source referenced by the original notebooks: <https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/4Z1fwRR295-1O3PMQBH6Dg/images-dataSAT.tar>. Place the archive locally at `data/raw/images-dataSAT.tar` and extract it under `data/raw/` so the `images_dataSAT/` directory contains the two class folders.


**Dataset inventory and license limitations:** Download access has been confirmed, but the archive's total/per-class counts, native image characteristics, and integrity have not been independently verified (these checks were skipped by explicit project decision). The license and redistribution/commercial-use rights are unknown. Do not commit or redistribute the dataset. See [`docs/dataset_provenance.md`](docs/dataset_provenance.md) and [`data/README.md`](data/README.md) for details.
