# 383: Predicting Water Suface Elevation in Ground Water

## Authors
1) [Luis Navarro](mailto:lunavarro@csumb.edu)
2) [Jose Alvarado](mailto:josalvarado@csumb.edu)
3) [Cory Griffiths](mailto:cgriffiths@csumb.edu)
4) [Anthony Doolan](mailto:adoolan@csumb.edu)

## Introduction
The dataset contains information about “Continuous groundwater level measurements aggregated to monthly time step.” It dates from December 1, 1969, through January 1, 2023. There are many stations in the data set, and each station can provide a groundwater measurement relative to the sea level and the station's elevation. There are 5 ways in which the water level is measured. This should help increase the quality of measurement when a particular device malfunctions. Each type of measurement comes with information about the quality control of the mechanism. The quality control appears to be good when the value is 1 and invalid when it is 255.

## What we are Trying to Predict
We can try to predict what the water level of the next 5 years will be for either 1 or a few measurement locations. For example station 21N02E26E005M has over 50 measurements going back to the 70's. This station has the most data that can predict what next years level is going to be. Take a look at the sectiion __"Graping the water Levels"__, you can see the cyclic variance of the water levels over the course of measurements. The cyclic nature of the measurements can be used to predict what next years water level will be based on the previous few years.

## Features
We are going to use the MSMT_DATE and STATION as the predictors for the water level. We need to convert the MSMT_DATE to a timestamp though.

### Column Information
* __STATION__: ID of the station, use var stations to get info based on id.
* __MSMT_DATE__: Date the measurement was taken. YYYY-MM-DD
* __WLM_RPE__: Water Level relative to reference point
* __WLM_RPE_QC__: Quality Control for above
* __WLM_GSE__: Water Level relative to ground surface elevation
* __WLM_GSE_QC__: Quality Control for above
* __RPE_WSE__: Water Surface Elevation relative to reference point
* __RPE_WSE_QC__: Quality Control for above
* __GSE_WSE__: Water surface elevation relative to ground surface elevation.
* __GSE_WSE_QC__: Quality Control for above
* __WSE__: water surface elevation
* __WSE_QC__: Quality Control for above