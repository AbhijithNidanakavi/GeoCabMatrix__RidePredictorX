# GeoCabMatrix__RidePredictorX
An advanced predictive model designed to forecast the number of taxi rides for any given location at any specific times of the day for NYC. The model utilizes sophisticated data analysis techniques to accurately anticipate ride demand, enabling taxi companies to strategically allocate their resources.
The implementation of this model significantly enhances the operational efficiency of taxi companies. It ensures a more dynamic and responsive service by predicting and meeting the fluctuating demands for rides. This not only improves customer satisfaction by reducing wait times but also optimizes the fleet usage, leading to increased profitability and resource management efficiency.

![GeoCabMatrix Web App Image](https://github.com/AbhijithNidanakavi/GeoCabMatrix__RidePredictorX/assets/91921508/d1c4b7b7-a550-4491-9a55-f92c36aa03d4)


Forecasting the upcoming hour's demand for NYC taxis, optimizing fleet distribution and revenue generation. This guide provides a comprehensive overview of project setup, execution, and continuous improvement.

# Table of Contents 
 * Application Overview
 * Features/Training/Inference Pipelines
 * Code Structure
 * Installation

## Application Overview : 
The application utilizes a trained LightGBM model to anticipate taxi demands for the forthcoming hour. It accesses data stored in a Feature Store on HopsWorks, containing records from January 2022 onwards. Additionally, GitHub Actions fetches updated data every 60 minutes.


## Features/Training/Inference Pipelines :
Employing the MLOps approach, this project adopts the FTI (Feature, Training, Inference) architecture, pioneered by Jim Dowling (CEO and Co-Founder of HopsWorks). This architecture provides a cohesive framework that encompasses both batch and real-time ML systems, organizing operations into three distinct pipelines.
A crucial aspect of the development journey involves prototyping and experimentation. Google Colab | Jupyter notebooks | Visual Studio serve as the cornerstone for these activities within this project. Here's an overview of the notebooks corresponding to each of the FTI pipelines:

![NYC pipeline](https://github.com/AbhijithNidanakavi/GeoCabMatrix__RidePredictorX/assets/91921508/cf962699-ac39-4b67-a4e9-c8e5e01a2018) 

### Features Pipeline :
Within the feature pipeline, a systematic approach is taken to fetch, transform, and store refined time-series taxi data, ensuring its readiness for utilization by machine learning models and other analytical endeavors.

### Training Pipeline : 
The Training Pipeline encompasses the establishment of data infrastructure, preprocessing, feature extraction, model training, and hyperparameter tuning, all aimed at crafting a resilient machine learning model.

### Inference Pipeline :
The Inference Pipeline is designed to fetch the most recent data, preprocess it, employ a pre-trained model for prediction, and efficiently store the outputs for downstream applications.


## Code Structure :
The project maintains a well-structured directory layout, promoting clarity, modularity, and seamless navigation. Below is an outline of the structure:
.
├── README.md                     - provides an overview of the project

│   ├── raw                       - contains the raw, unprocessed ride data.
│   │   ├── rides_2022-01.parquet 
│   │   ├── rides_2022-02.parquet 
│   │   └── ...
│   └── transformed               - contains datasets that have undergone some form of processing
│       ├── tabular_data.parquet  
│       ├── ts_data_rides_2022_01.parquet  
│       └── validated_rides_2022_01.parquet 
│       └── ... 
├── models                        - any machine learning models.
├── notebooks                     - exploratory and developmental Jupyter notebooks.
│   ├── 01_load_and_validate_raw_data.ipynb
│   ├── 02_transform_raw_data_into_ts_data.ipynb
│   ├── 03_transform_ts_data_into_features_and_targets.ipynb
│   ├── ...
├── pyproject.toml                - project metadata and dependencies
├── scripts                       - scripts for automation, data collection, and other utilities.
├── src                           - directory containing reusable code, functions, and classes.
└── tests                         - test scripts for functionalities

## Installation : 
To get underway, clone this repository and establish the environment:

