# Traffic Sign Recognition System

## Overview

This repository contains a comprehensive Traffic Sign Recognition (TSR) system that demonstrates state-of-the-art techniques in object detection and classification. The system utilizes YOLOv8 for detection and a hybrid approach combining VGG16 and Random Forest for classification. This project showcases various aspects of the machine learning pipeline, including data exploration, preprocessing, embedding model comparisons, and model evaluations.

## Table of Contents

1. [Features](#features)
2. [Project Structure](#project-structure)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Modules](#modules)

## Features

- Demo application for real-time traffic sign detection and classification
- Exploratory Data Analysis (EDA) of traffic sign datasets
- Data preprocessing and augmentation techniques
- Comparison of various embedding models
- 3D visualization of embedding clusters
- Evaluation and comparison of multiple classification models
- YOLOv8-based traffic sign detection
- Integration of Hough Circle Transform for speed limit sign detection
- Optical Character Recognition (OCR) using TrOCR for speed limit value extraction

## Project Structure

```
TSR/
│
├── data/
│   ├── raw_dataset/
│   └── processed/
│
├── models/
│   ├── detection/
│   ├── classification/
│   └── embeddings/
│
├── notebooks/
|   ├── YOLO.ipynb
│   ├── EDA.ipynb
│   ├── Preprocessing.ipynb
│   ├── Embedding_Comparison.ipynb
│   └── Model_Training.ipynb
│
├── src/
|   ├── app.py
|   └── utils/
│
├── requirements.txt
│
└── README.md
```

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/AkhilVaidya91/Signumum-Revelio.git
   cd Signumum-Revelio
   ```

2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

## Usage

1. Run the main application:
   ```
   streamlit run app.py
   ```

2. Open your web browser and navigate to `http://localhost:5000` to access the landing page and demo application.

3. To explore the individual components of the project, refer to the Jupyter notebooks in the `notebooks/` directory.

## Modules

### Landing Page and Demo

The landing page provides an overview of the project and includes a demo where users can select from a set of sample images to see the traffic sign detection and classification in action.

### Data Exploration and Preprocessing

- `notebooks/EDA.ipynb`: Exploratory Data Analysis of the traffic sign datasets
- `notebooks/Preprocessing.ipynb`: Data preprocessing techniques, including augmentation and balancing

### Embedding Models

- `notebooks/Embedding_Comparison.ipynb`: Comparison of various embedding models, including VGG16, Resnet-50 etc.
- `notebooks/Embedding_Viz.ipynb`: 3D visualization of embedding clusters

### Classification Models

- `notebooks/Model_Training.ipynb`: Training and evaluation of multiple classification models
- `src/utils/classifier.py`: Implementation of the hybrid VGG16 + Random Forest classifier

### Detection Model

- `src/utils/detector.py`: YOLOv8-based traffic sign detection model
- `src/utils/hough_transform.py`: Hough Circle Transform for speed limit sign detection

### OCR

- `src/utils/ocr.py`: TrOCR implementation for speed limit value extraction