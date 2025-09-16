# mTBILR - Includes Both Athlete and External Cohort

Linear Regression (LR) models developed for Cohort 1 and 2 of the metabolic biomarker data provided by Fiandaca et al., 2019. Serves as a control, as an LR model has a simple structure.  
In Cohort 1, the value '0' indicates a control (no mTBI) and the value '6' indicates a test (positive mTBI). In Cohort 2, the value '0' indicates a control, and the value '1' indicates a test. Per Fiandaca and colleagues, data collected for Cohort 1 was done so 6 hours post-injury, and all data for Cohort 2 was collected at various times post-injury (no control for data collection).  
See files: "AthleteTBI.csv" and "ExternalTBI.csv"

# How It's Made

**_Language_**
- Python v3.9.21
  
**_IDE_**
- Jupyter Notebook
  
**_Libraries Used_**
- Pandas - data organization/cleaning
- NumPy - support for dataframe
- scikit-learn - basis of network (training/testing split, declaration, performance report)
- seaborn - data visualization


# Workflow
- Importing/pre-processing/cleaning data
     - NOTE: Cohort 1 dataset included a misspelling; "OriiginalGroupID", hence the misspelling in the code.
- Training/testing split -> 80/20
- Training/testing phase (implemented using scikit-learn)
- Output of performance metrics (see below)

# Performance Metrics at a Glance  
__Testing Metrics__  
<img width="1126" height="252" alt="image" src="https://github.com/user-attachments/assets/0001f97b-a640-4fce-86c9-52cd066ef586" />  
Note: Athlete Cohort refers to Cohort 1, and External Cohort refers to Cohort 2.

Accuracy of Cohort 1: 0.54  
Accuracy of Cohort 2: 0.75  

# Final Notes  
It can be concluded, due to the lack of performance by the linear regression (LR) models in comparison to the multi-layer perceptron (MLP) models, that the data is best modeled by a more complex structure such as an MLP. Future work should seek to use higher-quality datasets and to ensure that similar workflows are followed across the models being developed. For example, the LR model does not assess an expanded datset like the MLP models do. Rather, it is limited to the original datset size. These limitations must be considered when interepreting the data, and future studies should seek to control this more appropriately. Ultimately, the LR models had a much lower accuracy than the MLP models do, suggesting the conclusion that MLP models are much more suited to model this biomarker data.

Link to Datasets:
https://datadryad.org/dataset/doi:10.5061/dryad.559907q  
Link to study where networks deployed:
https://docs.google.com/document/d/1jEtMAgtlKWKamzhPKkx_7q6fxsLvOcL7hpjEeVZ624Y/edit?usp=sharing
