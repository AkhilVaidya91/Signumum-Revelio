# Traffic Sign Recognition (Notebooks Collection)

## Overview

This repository is a notebooks-first collection of experiments and pipelines for Traffic Sign Recognition (TSR). It contains Jupyter notebooks for exploratory data analysis, preprocessing, embedding experiments, classification training/evaluation, and YOLO-based detection experiments.

## Table of Contents

1. [Features](#features)
1. [Project structure](#project-structure)
1. [Installation](#installation)
1. [How to use](#how-to-use)
1. [Notes & Contributing](#notes--contributing)

## Features

- Collection of Jupyter notebooks covering EDA, preprocessing, embeddings, classification and detection
- YOLO-based detection experiments (configuration and dataset layout under `data/detection-YOLO/`)
- Classification experiments (notebooks use the dataset under `data/classification/`)
- Utilities in `utils/` to support notebooks

## Project structure

The repository is organized around data and notebooks. Important top-level files and folders:

```text
.
├── data/
│   ├── assets/                # example images and assets
│   ├── classification/        # image folders per class (0, 1, 2, ...)
│   └── detection-YOLO/        # YOLO dataset config and splits (classes.txt, data_custom.yaml, train/, val/)

├── notebooks/                 # Jupyter notebooks (primary entry points for experiments)
│   ├── classification_training.ipynb
│   ├── CNN_CBAM_EXPERIMENTAL.ipynb
│   ├── data_preproc.ipynb
│   ├── detection.ipynb
│   ├── EDA.ipynb
│   └── embedding.ipynb

├── requirements.txt           # Python dependencies
└── README.md                  # this file
```

If you'd like a quick file listing of the notebooks in your clone, see the `notebooks/` directory.

## Installation

1. Clone the repository:

```powershell
git clone https://github.com/AkhilVaidya91/Traffic-Sign-Recognition.git
cd "Traffic-Sign-Recognition"
```

1. Create and activate a Python virtual environment (optional, recommended):

```powershell
python -m venv .venv; .\.venv\Scripts\Activate.ps1
```

1. Install Python dependencies:

```powershell
pip install -r requirements.txt
```

Notes:

- The notebooks may rely on packages listed in `requirements.txt`. If you prefer, open the notebooks in a cloud environment (Colab) and install only the packages you need there.

## How to use

Open the notebooks with Jupyter, JupyterLab, or VS Code (Notebook editor). Typical steps:

1. Start JupyterLab or Jupyter Notebook:

```powershell
jupyter lab
```

1. Open any notebook from the `notebooks/` folder. Recommended starting points:

- `EDA.ipynb` — exploratory data analysis of the dataset
- `data_preproc.ipynb` — preprocessing and dataset preparation
- `embedding.ipynb` — embedding/model comparison experiments
- `classification_training.ipynb` — classification model training and evaluation
- `detection.ipynb` — YOLO-based detection experiments (uses `data/detection-YOLO/`)

1. Detection training: the `data/detection-YOLO/` folder contains a `data_custom.yaml` and `classes.txt` and train/val splits. Follow the `detection.ipynb` notebook which documents how to run training/evaluation (Ultralytics/YOLO training is commonly run from a notebook cell or the command line).

## License

See the `LICENSE` file in the repository for licensing information.

---
