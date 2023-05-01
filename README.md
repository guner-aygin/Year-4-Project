# Year-4-Project

This is the culmination of my physics master's project titled **Predicting Solar Cycles using Probabilistic Machine Learning**. This project was around 7 months long, and was completed with the aid of my supervisor Dr Guy Davies. The key methods used for this project was **Gaussian processes** $\mathcal{GP}$ regression.

The goal of this project was to test various probabilistic ML techniques to assess whether it was possible to obtain suitable predictions for future solar cycles. The main data used for this project was the **daily sunspot number** data between 1818 and 2023 (https://www.sidc.be/silso/infosndtot), which was smoothed using a **Savitzky-Golay filter**. This smoothed data was used for all other modelling applications used throughout this project, and can be found in the *Sunspot Data Plotting* document.

***
All project logs can be found in *Project Notebook*, with the main results in *Model Evaluation*
***

There are many example notebooks in this repository which demonstrate how the various ML techniques can be used, including a GIF of how a $\mathcal{GP}$ learns from data. All of these codes can be found in the *Examples* folder. 

The work from this project was used to establish that there was no statistically significant relationship between the amplitude of a solar cycle and the descending time of a cycle 3 cycles earlier (*LinReg_DT*).

Neural networks were tried and tested, however due to the project deadline they had to be abandoned at the very end, because no suitable predictions were made with them. Stellar cycles were also considered for modelling, but again due to time constraints were abandoned. 

***

The most important notebooks are in *Full Cycle Modelling/Gaussian Processes*

Mulitple $\mathcal{GP}$ kernel combinations were experimented with to find the one which produced the most accurate forecasts, with the **Matern 5/2 $\times$ Periodic** kernel coming out on top. However, the models were found to only forecast well becasue the **sine-squared** mean function chosen was able to successfully capture the long term trend. Without this mean our predictions were found to very quickly falter.

It can be concluded that $\mathcal{GP}$s may show very good promise at predicting solar cycled in the near term, but as of yet cannot be used for long-term forecasts. SC 25 was forecast, with the results given in *Model Evaluation*.





