RECol Study Results:
=====================

This repository contains the code to obtain results of RECol paper and notebook 
to understand the RECol approach with a Toy example. RECol is a pre-processing 
step, applied before running a standard outlier detection (OD) machine learning algorihm 
on a dataset to improve its results compared to standard (Novel) OD approach.
Unlike other OD approaches RECol helps to detect the deviations in the data by 
focusing on underlying relationships within the data features. In perticular, it 
map the given data to a reconstruction error space by computing recosntruction error 
from a supervised model where one feature is used as label and all other features as input
in leave one out fashion. This enables the algorithms to easily identify data points that 
can hardly be reconstructedby the relationships in the data.

For more information please refer the original paper.

Note: 
- Dataset link: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/OPQMVF
- For using the dataset please cite:
@article{goldstein,
    author = {Goldstein, Markus AND Uchida, Seiichi},
    journal = {PLOS ONE},
    publisher = {Public Library of Science},
    title = {A Comparative Evaluation of Unsupervised Anomaly Detection Algorithms for Multivariate Data},
    year = {2016},
    month = {04},
    volume = {11},
    url = {https://doi.org/10.1371/journal.pone.0152173},
    pages = {1-31},
    doi = {10.1371/journal.pone.0152173}
}

Repository Structure
--------------------

- RECol_Paper_Toy_Example.ipynb: Simulation of RECOL and Baseline approaches on a 2D example dataset.
- RECol_Approach_Result_Evaluation_using_ROC-AUC.ipynb: Detailed Analysis of RECol output on ROC-AUC metric, 
includes tables and plots shown in the original paper. 
- RECol_Approach_Result_Evaluation_using_PR-AUC.ipynb: Detailed Analysis of RECol output on ROC-AUC metric, 
includes tables and plots shown in the original paper.
- Result: Contains experimental results of Baseline OD models and RECol method.
> - Best_Baseline_model_Output: Result of all the baseline od models (referred from M. Goldstein) mentioned in the paper
> - RECol_Output: Contains results of all 895 experiments conducted using different hyperparameters used for RECol approach.
> - RECol_Output_Kdd_v2: RECol output for kdd dataset. Includes 8 experiment results.
> - RECol_Output_v2_scores: Conains accuary scores of supervised models used to compute reconstruction error columns in RECol approach. 


Requirements
------------

To run this code, we recommend:
- Laptop/desktop with CPU (GPU not required)
- minimum 4 GB free RAM
- Linux/Ubuntu 64 bit with Python 2.7/3.5


Required Packages
-----------------

- sklearn >= 0.21.0
- numpy >= 1.18.1 
- scipy >= 1.3.2
- statsmodels >= 0.12.2
- pyod >= 0.7.9
- pandas >= 0.25.3
- matplotlib >= 3.1.1
- seaborn >= 0.10.0


For Running the Code
--------------------

- Download the zip file and extract.
- cd RECol-master
- start jupyter notebook and open .ipynb files


Contributors
------------
