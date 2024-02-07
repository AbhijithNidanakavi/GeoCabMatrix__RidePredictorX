# GeoCabMatrix__RidePredictorX
An advanced predictive model designed to forecast the number of taxi rides for any given location at any specific times of the day for NYC.

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


