<div align="left" style="position: relative;">

<img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/ec559a9f6bfd399b82bb44393651661b08aaf7ba/icons/folder-markdown-open.svg" align="right" width="30%" style="margin: -20px 0 0 20px;">

<h1>CHURN-PREDICTION</h1>

<p align="left">

<em>A customer churn prediction system using Artificial Neural Networks</em>

</p>

<p align="left">

  <img src="https://img.shields.io/github/license/hemanthdatta/churn-prediction?style=default&logo=opensourceinitiative&logoColor=white&color=00ff36" alt="license">

  <img src="https://img.shields.io/github/last-commit/hemanthdatta/churn-prediction?style=default&logo=git&logoColor=white&color=00ff36" alt="last-commit">

  <img src="https://img.shields.io/github/languages/top/hemanthdatta/churn-prediction?style=default&color=00ff36" alt="repo-top-language">

  <img src="https://img.shields.io/github/languages/count/hemanthdatta/churn-prediction?style=default&color=00ff36" alt="repo-language-count">

</p>

</div>

<br clear="right">

## Table of Contents

* [Overview](#-overview)
* [Features](#-features)
* [Project Structure](#-project-structure)

  * [File Index](#file-index)
* [Getting Started](#-getting-started)

  * [Prerequisites](#-prerequisites)
  * [Installation](#-installation)
  * [Usage](#-usage)
  * [Testing](#-testing)
* [Project Roadmap](#-project-roadmap)
* [Contributing](#-contributing)
* [License](#-license)
* [Acknowledgments](#-acknowledgments)

---

## Overview

The **Churn-Prediction** project aims to predict whether customers will leave a service or product based on historical data. Leveraging data preprocessing, exploratory analysis, and an Artificial Neural Network (ANN), this system provides insights into key factors driving churn and delivers a web-based interface for easy predictions.

---

## Features

* Comprehensive data preprocessing: handles missing values, encoding, and feature scaling.
* Exploratory Data Analysis (EDA) with interactive visualizations in Jupyter notebooks.
* Model training with a multilayer perceptron (ANN) tailored for binary classification.
* Hyperparameter tuning using grid and randomized search to optimize model performance.
* Deployment-ready Flask app (`app.py`) for real-time prediction via REST API or simple web form.
* Logging and experiment tracking with TensorBoard events under `logs/`.

---

## Project Structure

```sh
churn-prediction/
├── Churn_Modelling.csv         # Dataset of historical customer records
├── app.py                      # Flask application for model serving
├── experiments.ipynb           # EDA and baseline model experiments
├── hyperparametertuningann.ipynb  # Hyperparameter tuning experiments for the ANN
├── label_encoder_gender.pkl    # Pre-trained label encoder for gender
├── logs/                       # TensorBoard logs for training and validation
│   └── fit
├── model.h5                    # Trained ANN model weights
├── onehot_encoder_geo.pkl      # Pre-trained encoder for geographical data
├── prediction.ipynb            # Interactive notebook for individual predictions
├── requirements.txt            # Python package dependencies
├── salaryregression.ipynb      # Example salary regression exercise
└── scaler.pkl                  # Pre-trained StandardScaler object
```

### File Index

| File                              | Description                                                        |
| --------------------------------- | ------------------------------------------------------------------ |
| **app.py**                        | Flask-based web service to load the model and serve predictions.   |
| **prediction.ipynb**              | Notebook demonstrating how to run single-record predictions.       |
| **hyperparametertuningann.ipynb** | Experiment notebook for tuning ANN hyperparameters.                |
| **salaryregression.ipynb**        | Auxiliary notebook showcasing salary regression example.           |
| **requirements.txt**              | Lists all Python dependencies required to run the project.         |
| **experiments.ipynb**             | Notebook containing EDA, feature engineering, and baseline models. |

---

## Getting Started

Follow these instructions to set up and run the churn prediction system locally.

### Prerequisites

* Python 3.8 or higher
* Pip package manager

### Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/hemanthdatta/churn-prediction.git
   cd churn-prediction
   ```

2. Install dependencies:

   ```sh
   pip install -r requirements.txt
   ```

### Usage

1. Start the Flask app:

   ```sh
   python app.py
   ```

2. Open your browser at `http://127.0.0.1:5000` to access the prediction form or send POST requests to `/predict` endpoint with JSON payload.

### Testing

Run unit and integration tests using pytest:

```sh
pytest --maxfail=1 --disable-warnings -q
```

---

## Project Roadmap

* [x] **Task 1**: Implement data preprocessing and baseline model.
* [ ] **Task 2**: Develop and optimize ANN architecture.
* [ ] **Task 3**: Deploy web service and write API tests.

---

## Contributing

Thanks for your interest in contributing! Please follow these steps:

1. Fork the repository on GitHub.
2. Create a new feature branch: `git checkout -b feature-name`.
3. Make your changes and commit: `git commit -m "Describe your changes"`.
4. Push to your fork: `git push origin feature-name`.
5. Open a pull request against the `main` branch.

See [CONTRIBUTING.md](https://github.com/hemanthdatta/churn-prediction/blob/main/CONTRIBUTING.md) for full guidelines.

---

## License

This project is licensed under the **MIT License**. See the [LICENSE](https://choosealicense.com/licenses/mit/) file for details.

---

## Acknowledgments

* Based on the original customer churn dataset from Kaggle.
* Inspired by tutorials from Towards Data Science and Machine Learning Mastery.
* Logo and icons courtesy of VSCode Material Icon Theme and Shields.io.
