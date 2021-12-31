## Iris Data Analysis in R
![made-with-R](https://img.shields.io/badge/Made%20with-R-1f425f.svg)
![plotly](https://img.shields.io/badge/plotly-007ACC?style=flat-square&logo=plotly&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyterlab-F37626?style=flat-square&logo=Jupyter&logoColor=white)

### Dataset Description:-
This Data was optained from The Global Terrorism Database (GTD) which is an open-source database that contains information about the terrorist attacks around the world from 1970 to 2017. The GTD includes the information about domestic and international terrorist incidents that have occured during this time periods and now includes more than 180,000 attacks. The database is maintained by researchers at the National Consortium for the Study of Terrorism and Responses to Terrorism, headquartered at the University of Maryland. In this dataset, there are a lot of missing observations which we cannot clean as it is a sensitive topic, so we leave it as it is.

### To load all required packages:- 
```r
library(dplyr)
library(ggplot2)
library(plotly)
library(countrycode)
library(viridisLite)
library(highcharter)
```

### To install all required packages:- 
```r
install.packages(c("ggplot2", "countrycode", "plotly", 
                   "dplyr", "viridisLite", "highcharter"))
```

### Some of the Output Images:- 
#### Bar Chart
<img align="center" src="https://github.com/PrakashAnalyst/LGMVIP-DataScience/blob/main/Task%204/images/bar.gif">

#### Histogram
<img align="center" src="https://github.com/PrakashAnalyst/LGMVIP-DataScience/blob/main/Task%204/images/hist.gif">

#### Density Plot
<img align="center" src="https://github.com/PrakashAnalyst/LGMVIP-DataScience/blob/main/Task%204/images/kde.gif">

#### Choropleth Map
<img align="center" src="https://github.com/PrakashAnalyst/LGMVIP-DataScience/blob/main/Task%204/images/map.gif">
