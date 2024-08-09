# Design

This study aims to research the measurment properties of Economic, Social, and Cultural Status (ESCS) using the 2018 data of the Programme for International Student Assessement (PISA).
It does so using three questions: 

1) To what extent is ESCS subject to measurement variance? This is researched using multigroup confirmatory factor analysis and alignment optimization. 

2) Can ESCS be modelled differently to reduce measurement variance and to better handle missing data? This is also researched using multigroup confirmatory factor analysis,
in addition to a simulation study and IRT analysis.  

3) Does this improved model of ESCS lead to a different estimate of the relation between ESCS and cognitive outcome variables? This is researched using linear regression. 

# Data

The data from the PISA 2018 student questionnaire is used. As this dataset is to large to be uploaded to GitHub, the dataset (called "CY07_MSU_STU_QQQ.sav") can be found via [this link](https://www.oecd.org/pisa/data/2018database/) 
or directly dowloaded via [this link](https://www.oecd.org/content/dam/oecd/en/data/datasets/pisa/pisa-2018-datasets/ssas-sps-data-files/SPSS_STU_QQQ.zip). This dataset includes responses 
of 612,004 students from 80 countries.

The datafile that can be found in the data folder in this archive (pisa18_m.RDS) contains the information about the mathematics ability of the students. It is used to investigate the third 
research question. This datafile is created using a script made and owned by Remco Feskens. To obtain this script, he can be contacted at remco.feskens@cito.nl. 

# Scripts

To follow the order as discussed in the master's thesis, the scripts should be run in the following order:

[RQ1_Recreation_ESCS.Rmd](https://github.com/kirstenvankessel/masterthesis/blob/main/scripts/RQ1_Recreation_ESCS.Rmd) - In this script the variables ESCS is recreated, as to check if we 
have a clear understanding of how ESCS is measured.

RQ1_meas_invar_mgcfa.Rmd - In this script the multigroup confirmatory factor analysis is performed to check for measurement invariance. The modification indices are inspected and model
parameters are changes as to minimize measurement invariance. 

RQ1_meas_invar_align.Rmd - In this script alignment optimization is performed to check for measurement invariance. 

RQ2_imputation_loop.Rmd - In this script the simulation study is performed. Note that we do not simulate data. The same dataset is used, but samples of complete cases are taken and values are
artificially made to be missing. This is done to inspect how well the imputation methods perform. The imputation methods are 1) Not imputing, 2) Stochastic regression imputation, and 3) 
Multiple imputation. 

RQ2_bottomup.Rmd - In this script IRT analysis is performed to inspect if the model can be improved on the level of the items. 

RQ3_relation.Rmd - In this script two new measures of ESCS are tested against the original measure of ESCS in PISA. 

# Ethics

Ethical approval for the study is obtained from the Utrecht University Ethics Review Board of the Faculty of Social and Behavioral Sciences (case number 23-1790). The data used is 
open access and anonymous. 

# Permission and access

This research archive is publicly available and can be accessed via [GitHub](https://github.com/kirstenvankessel/masterthesis). I, Kirsten van Kessel, am solely responsible for this research achive 
and can be contacted via k.d.vankessel@students.uu.nl. 

Kirsten van Kessel 
12-08-2024

