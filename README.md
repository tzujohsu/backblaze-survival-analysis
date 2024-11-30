## Survival analysis and lifespan modeling

Hard disk drives are essential storage devices used in computers and servers. Selecting the right hard drive is important and challenging because hard disk can lead to data loss and operational disruptions. A cloud storage and backup company, Backblaze has provided quality source data and summary statistics of hard drive failure rates from their datacenter. This report applies survival analysis techniques to uncover patterns and inform storage infrastructure decisions.

* The analysis draws from [Backblaze's Hard Drive Data and Stats](https://www.backblaze.com/cloud-storage/resources/hard-drive-test-data) from 2016-2023, these logs capture daily snapshots of optional drive and their S.M.A.R.T. (Self-Monitoring, Analysis, and Reporting Technology) statistics reported by that drive.
* After preprocessing steps, the dataset comprises 388,299 unique drive combinations from Hitachi, Toshiba, Western Digital, and Seagate, the top 4 manufacturers from their logs.
* The analysis is conducted using R's survival analysis packages ‘survival’, ‘survminer’, ‘gtsummary’
* The nonparametric method Kaplan-Meier estimation and semi-parametric method Cox regression are employed to examine how manufacturer, drive capacity, and SMART attributes influence drive reliability.

[![](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)](https://www.r-project.org) [![](https://img.shields.io/badge/Tidyverse-25283D?style=for-the-badge&logoColor=white)](https://www.tidyverse.org/) [![](https://img.shields.io/badge/survival-7C98B3?style=for-the-badge&logoColor=white)](https://cran.r-project.org/web/packages/survival/index.html) [![](https://img.shields.io/badge/survminer-B5D6B2?style=for-the-badge&logoColor=white)](https://github.com/kassambara/survminer) 

<p align="center">
    <img src="KM_survival_curve.png" alt="KM result">
</p>
