# Fault-Detection-Using-Vibrational-Data
### Overview
This repository contains a fault detection project that leverages vibrational data collected from IoT sensors on industrial machines. The primary objective is to identify faulty data that indicates when maintenance is required. This is achieved through clustering techniques, specifically DBSCAN (Density-Based Spatial Clustering of Applications with Noise), to detect and flag noisy data points that signify potential faults.

## Project Steps
### Data Collection
The vibrational data was collected using IoT sensors installed on various machines. The dataset includes time-series data that records the intensity and patterns of vibrations over a period of time.

### Data Preprocessing
To prepare the data for analysis, several preprocessing steps were carried out :

Loading Data: The vibrational data is loaded from a CSV file.

Cleaning Data: Any irrelevant or missing data is handled to ensure the dataset is clean and ready for analysis.

Normalization: The data is normalized to bring all values into a comparable range, which is essential for clustering algorithms.

### Clustering with DBSCAN
DBSCAN is used to cluster the data and identify noisy data points :

DBSCAN: This clustering technique is particularly useful for identifying noise in datasets with varying densities.

Parameter Tuning: The parameters eps (maximum distance between two samples) and min_samples (minimum number of samples in a neighborhood) are tuned to optimize the clustering performance.

### Fault Detection
Noisy data points identified by DBSCAN are flagged as potential faults :

Flagging Faults: Data points classified as noise (Cluster = -1) are considered faulty.

Maintenance Alerts: These faults indicate when maintenance might be required, helping in predictive maintenance strategies.
