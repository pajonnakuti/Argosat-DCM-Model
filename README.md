# Estimate Deep Chlorophyll Maxima from D26 Isotherm using Machine Learning (Argosat-DCM-Model)

This repository contains code and resources for estimating the Deep Chlorophyll Maxima (DCM) depth using the D26 isotherm as a proxy and leveraging machine learning with Argo float and satellite data.

## Project Overview

The Deep Chlorophyll Maximum (DCM) is a crucial feature in the ocean, representing a layer of concentrated phytoplankton.  Accurate DCM depth estimation is vital for understanding marine primary productivity and carbon cycling. This project aims to improve DCM depth estimation by combining the relationship between the D26 isotherm and DCM depth with machine learning, incorporating readily available Argo float and satellite data.

## Data Sources

*   **Argo Float Data:** Temperature, salinity, pressure, and chlorophyll profiles.
*   **Satellite Data:** Sea Surface Temperature (SST), Chlorophyll-a concentration, Sea Level Anomaly (SLA), and potentially Mixed Layer Depth (MLD).

## Methodology

1.  **Data Acquisition and Preprocessing:** Downloading, cleaning, and merging Argo and satellite data.
2.  **Feature Engineering:** Creating relevant features from the combined dataset.
3.  **Model Selection and Training:** Choosing and training a suitable machine learning model (e.g., regression models, neural networks).
4.  **Model Evaluation and Validation:** Assessing model performance using appropriate metrics.
5.  **DCM Depth Estimation:** Applying the trained model to predict DCM depth.

## Repository Structure

├── data/          # Contains raw and processed data (not included in the repo due to size)
│   ├── argo/      # Argo float data
│   └── satellite/ # Satellite data
├── notebooks/     # Jupyter notebooks for data processing, model training, and analysis
│   ├── data_preprocessing.ipynb
│   ├── feature_engineering.ipynb
│   ├── model_training.ipynb
│   └── model_evaluation.ipynb
├── scripts/       # Python scripts for specific tasks (optional)
│   └── download_data.py
├── outputs/       # Stores model outputs, figures, and other results
├── README.md      # This file
├── requirements.txt # List of required Python packages
└── environment.yml # Conda environment file (optional)

**Description:**

*   **`data/`:** This directory holds the raw and processed data.  The `argo/` subdirectory contains Argo float data, and the `satellite/` subdirectory contains satellite data.  *Note: Due to their size, these datasets are not included directly in the repository.  See the "Getting Started" section for instructions on how to download the data.*
*   **`notebooks/`:** This directory contains Jupyter notebooks used for data processing (`data_preprocessing.ipynb`), feature engineering (`feature_engineering.ipynb`), model training (`model_training.ipynb`), and model evaluation (`model_evaluation.ipynb`).
*   **`scripts/`:**  This directory contains any Python scripts used for specific tasks, such as downloading data (`download_data.py`). This directory is optional.
*   **`outputs/`:** This directory stores the analysis results, including model outputs, figures, and other generated files.
*   **`README.md`:** This file (the one you are reading) provides an overview of the project and instructions for getting started.
*   **`requirements.txt`:** This file lists the required Python packages for the project.  You can install these using `pip install -r requirements.txt`.
*   **`environment.yml`:** (Optional) This file specifies a Conda environment for the project. You can create the environment using `conda env create -f environment.yml`.


## Requirements

*   Python 3.x
*   Required Python packages (install using `pip install -r requirements.txt` or `conda env create -f environment.yml`) - See `requirements.txt` for a detailed list.  Key packages include:
    *   `numpy`
    *   `pandas`
    *   `scikit-learn`
    *   `xarray`
    *   `matplotlib`
    *   `cartopy`
    *   `tensorflow` or `pytorch` (if using neural networks)

## Getting Started

1.  Clone the repository: `git clone https://github.com/[your_username]/[repository_name].git`
2.  Navigate to the repository: `cd [repository_name]`
3.  Create a virtual environment (recommended): `python3 -m venv .venv` (or `conda create -n myenv python=3.9`)
4.  Activate the environment: `source .venv/bin/activate` (or `conda activate myenv`)
5.  Install the required packages: `pip install -r requirements.txt` (or `conda env update -f environment.yml`)
6.  Download the Argo and satellite data (due to size, these are not included in the repository.  Scripts or instructions for downloading the data should be included in the `scripts/` directory or this README).  Place the data in the `data/` directory.
7.  Run the Jupyter notebooks in the `notebooks/` directory to reproduce the analysis and train the model.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

[Specify the license under which the code is distributed (INCOIS).]

## Contact
[Pavan Kumar Jonnakuti / pavankumar.j@incois.gov.in]
