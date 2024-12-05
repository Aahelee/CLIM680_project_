Assessing Variability in Historical and piControl Sea Surface Temperature Data Using Covariance Discriminant Analysis
---
## Introduction

Understanding the sources of Sea Surface Temperature (SST) variability is a crucial first step in unraveling the climate dynamics that drive it. In recent years, ocean temperatures have been rising globally. This project seeks to determine whether variability in model data differs significantly from that in piControl data. The method employed here can also be used to address questions such as when the variability becomes significantly different and what common patterns exist between the two datasets. Additionally, this approach can be applied at a local scale to investigate whether variability in specific study areas has changed.


The goal of the project is to test whether historical data exhibits more variability than the control run. If the historical data shows significantly greater variability, it would suggest an influence from external factors beyond internal processes.

•  **Historical Run**: A simulation of past climate conditions (e.g., 1850–present) using observed external forcings.

•  **Ensemble**: A set of model simulations with varied initial conditions or parameters to assess variability and uncertainty.

•  **piControl Run**: A pre-industrial control run simulating a stable climate with fixed pre-1850 forcings for baseline comparisons.

---
Data Description:
The dataset used is from CMIP6, utilizing the IPSL-CM5A2-INCA model. 

Source:
Available at https://aims2.llnl.gov/search

Spatial and Temporal Resolution:
Initial Resolution: 100km
Regirded into 1 degree
Initial Time Resolution: monthly
Converted into annual

Variable:
Sea Surface Temperature (SST).

Time Span:
The dataset covers the period from 1850 to 2014.

Data type: 
Historical10 ensembles
piControl

---
The goal of the project is to test whether historical data exhibits more variability than the control run. If the historical data shows significantly greater variability, it would suggest an influence from external factors beyond internal processes.

**Historical Run**: A simulation of past climate conditions (e.g., 1850–present) using observed external forcings.

**Ensemble**: A set of model simulations with varied initial conditions or parameters to assess variability and uncertainty.

**piControl Run**: A pre-industrial control run simulating a stable climate with fixed pre-1850 forcings for baseline comparisons.

---
## Results and Analysis

The dataset contains monthly values converted to annual Sea Surface Temperature (SST). Figure 1 illustrates the difference between the annual mean of the first ensemble and the annual mean of the piControl run across 25 years between 1850-2014. Over time, a progressively larger area shows warming characteristic of the historical run.

After importing SST data from 10 ensembles, they were combined with the control run to calculate Empirical Orthogonal Functions (EOFs). The patterns found are common to both historical and control runs, but the principal component (PC) time series differ. This calculation was performed for 50 ensembles. Notably, the first EOF does not explain the maximum variance of historical or piControl data. Instead, it maximizes the variance ratio between historical and piControl data. The first EOF resembles an El Niño pattern, while the second EOF shows a Pacific Decadal Oscillation pattern. Figure 2 displays the first 8 EOFs. 

![climatology](https://github.com/user-attachments/assets/e972a434-80fb-427c-b808-1afa19e7a14f)

Figure 1: Difference between the annual mean temperature of Historical data (1 ensmeble) and piControl data for different years.

[Jupyter Notebook Link](https://github.com/Aahelee/CLIM680_project_/blob/main/covariance_discriminant_analysis.ipynb)

---
After importing SST data from 10 ensembles, they were combined with the control run to calculate Empirical Orthogonal Functions (EOFs). The patterns found are common to both historical and control runs, but the principal component (PC) time series differ. This calculation was performed for 50 ensembles. Notably, the first EOF does not explain the maximum variance of historical or piControl data. Instead, it maximizes the variance ratio between historical and piControl data. The first EOF resembles an El Niño pattern, while the second EOF shows a Pacific Decadal Oscillation pattern. Figure 2 displays the first 8 EOFs. 

![pc3](https://github.com/user-attachments/assets/6e267686-96e8-4c3c-9559-6a5f590a504c)

Figure 2: The first 3 Principal Components Across 3 Ensembles and Control Run.

Figure 3 shows the PC time series for the first three EOFs across the control run and three ensemble members. The first PC exhibits visibly different variability compared to the control run. The second is more nuanced, and from the third onward, they begin to look more similar.

![eof8](https://github.com/user-attachments/assets/32a9a4f8-3c38-4edb-983d-6f0b16a889ea)

Figure 3: First Eight EOFs of the pooled SST Data.

---
Mutual information Criterion (MIC) was used to determine the optimal number of EOFs for comparison. The Maximum Information Criterion provides a systematic approach by balancing how well a model explains the data against the complexity of the model. The core philosophy is to balance two competing objectives: Model Complexity and Model Fit/Explanation of Variance. The Information Criteria method works by calculating how well the model explains the data and simultaneously penalizing the added number of parameter. It creates a score that combines these two aspects. Initially adding more parameter explains more variance while keeping the mic low. But after a certain points adding a new parameter adds more penalty than it explain the variance. Figure 4 shows the discrimination values for all 50 EOFs calculated. For this analysis the optimal number of EOF was found to be 10, where the data is best explained by the model. 

![dis](https://github.com/user-attachments/assets/eb871262-0bf4-4378-9538-37ca5f1ddfc6)

Figure 4: Criterion for selecting the number of EOFs

---
To test the significance of the variance ratios of the historical and piControl, a Monte Carlo test was done. The goal here is to understand if the differences you see between two datasets (historical and control in this case) are truly meaningful or just random noise. The Monte Carlo method runs a lot of “what if” scenarios to establish a baseline. A fairly large
Number of synthetic datasets are created that have similar statistical properties. By generating these random datasets and analyzing them, a "background noise" benchmark is created. When the variance ratio of the historical and control data are compared against this background of random variations, the results show which differences are statistically significant. The results show that only the variance ration for the first EOF was significantly different for historical and control run. Figure 5 shows the significance of the first 10 EOFs, which were the optimal number of EOFs. Only the first variance ratio is significantly hisher than the signicance range. The results imply that the variance ratio between the datasets are significant. In other they have significantly different variability, which has to an influence form external forcings. 

![var_ratio](https://github.com/user-attachments/assets/2ea2034d-16d6-4e3e-ad0e-5d85358db5a1)

Figure 5: Discriminant Ratios between historical and control simulations.

For a smaller ensemble of 3 members, the optimal EOF number was 7, with variance ratios being almost the same and significance found only in the first EOF.

[Jupyter Notebook Link](https://github.com/Aahelee/CLIM680_project_/blob/main/covariance_discriminant_analysis.ipynb)
---
## Summary 

This project explores the variability of Sea Surface Temperature (SST) using the IPSL-CM5A2-INCA model from CMIP6, comparing historical runs with pre-industrial control runs (piControl). The goal is to identify significant differences in SST variability and understand how external forcings influence these patterns.

Empirical Orthogonal Functions (EOFs) were calculated to capture dominant modes of variability in SST. The first EOF, resembling an El Niño pattern, was designed to maximize the variance ratio between historical and piControl runs rather than explaining the maximum variance in either dataset. Other EOFs, such as one resembling the Pacific Decadal Oscillation, reveal additional important patterns. Mutual Information Criterion (MIC) analysis determined that 10 EOFs optimally describe the variability in the dataset, balancing complexity with explanatory power. For smaller ensembles, the optimal number of EOFs was 7.

A Monte Carlo test was performed to evaluate the significance of variance ratios between the two datasets. This method generated random synthetic datasets to establish a baseline for "background noise." The results showed that only the variance ratio for the first EOF was significantly higher in the historical runs, indicating that external forcings, such as greenhouse gas emissions, likely drive this increased variability.

Limitation: The Monte Carlo test assumes the data is independent and identically distributed (i.i.d.), which is not true for annual mean SST data. The degree of freedom is lower than assumed, potentially broadening the actual significance limit and uncertainty range. A future improvement would be to employ a significance testing method that does not assume i.i.d. conditions.




