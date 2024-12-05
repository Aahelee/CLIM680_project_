title
---
Introduction

Understanding the sources of Sea Surface Temperature (SST) variability is a crucial first step in unraveling the climate dynamics that drive it. In recent years, ocean temperatures have been rising globally. This project seeks to determine whether variability in model data differs significantly from that in piControl data. The method employed here can also be used to address questions such as when the variability becomes significantly different and what common patterns exist between the two datasets. Additionally, this approach can be applied at a local scale to investigate whether variability in specific study areas has changed.
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

---
## Results and Analysis

The dataset contains monthly values converted to annual Sea Surface Temperature (SST). Figure 1 illustrates the difference between the annual mean of the first ensemble and the annual mean of the piControl run across 25 years between 1850-2014. Over time, a progressively larger area shows warming characteristic of the historical run.

After importing SST data from 10 ensembles, they were combined with the control run to calculate Empirical Orthogonal Functions (EOFs). The patterns found are common to both historical and control runs, but the principal component (PC) time series differ. This calculation was performed for 50 ensembles. Notably, the first EOF does not explain the maximum variance of historical or piControl data. Instead, it maximizes the variance ratio between historical and piControl data. The first EOF resembles an El Niño pattern, while the second EOF shows a Pacific Decadal Oscillation pattern. Figure 2 displays the first 8 EOFs. 


![random fig1](https://github.com/Aahelee/CLIM680_project_/blob/main/figures/climatology.png)

Figure: Difference between the annual mean temperature of Historical data (1 ensmeble) and piControl data for different years.


Figure: Difference between the annual mean temperature of Historical data (1 ensmeble) and piControl data for different years.
---
![fig3](https://github.com/Aahelee/CLIM680_project_/blob/main/figures/eof8.png)

Figure: Difference between the annual mean temperature of Historical data (1 ensmeble) and piControl data for different years.

After importing SST data from 10 ensembles, they were combined with the control run to calculate Empirical Orthogonal Functions (EOFs). The patterns found are common to both historical and control runs, but the principal component (PC) time series differ. This calculation was performed for 50 ensembles. Notably, the first EOF does not explain the maximum variance of historical or piControl data. Instead, it maximizes the variance ratio between historical and piControl data. The first EOF resembles an El Niño pattern, while the second EOF shows a Pacific Decadal Oscillation pattern. Figure 2 displays the first 8 EOFs. 

---

---
![random fig](https://github.com/Aahelee/CLIM680_project_/blob/main/figures/pc3.png)

Spatial and Temporal Resolution:
Initial Resolution: 100km
Regirded into 1 degree
Initial Time Resolution: monthly
Figure: Difference between the annual mean temperature of Historical data (1 ensmeble) and piControl data for different years.
Converted into annu
---
![random fig](https://github.com/Aahelee/CLIM680_project_/blob/main/figures/dis.png)


Spatial and Temporal Resolution:
Initial Resolution: 100km
Regirded into 1 degree
Initial Time Resolution: monthly
Figure: Difference between the annual mean temperature of Historical data (1 ensmeble) and piControl data for different years.
Converted into annu
---
![random fig](https://github.com/Aahelee/CLIM680_project_/blob/main/figures/var_ratio.png)

Spatial and Temporal Resolution:
Initial Resolution: 100km
Regirded into 1 degree
Initial Time Resolution: monthly
Figure: Difference between the annual mean temperature of Historical data (1 ensmeble) and piControl data for different years.
Converted into annu





