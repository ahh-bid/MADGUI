<p align="center">
  <img src="https://user-images.githubusercontent.com/108456770/223624233-e40b55fa-fa50-4b37-a608-31077630311a.png" alt= “madgui_logo” width="200" height="200" margin:auto;">
</p>

# MADGUI : Material Design Graphical User Interface 

<p style="text-align:justify;">
User-friendly Graphical User Interface (GUI) developed at the National Institute for Materials Science (NIMS, MaDIS) for performing statistical data analysis, machine learning (ML) modelisation, and composition/process optimisation through Bayesian optimisation.
</p>

Can be used directly with the link below:

Streamlit app:  https://lambard-ml-team-madgui.streamlit.app/

Code accessible on GitHub:

GitHub page: https://github.com/Lambard-ML-Team/MADGUI

### Developers:

Christophe BAJAN* & Guillaume LAMBARD*

**National Institute for Materials Science, Tsukuba, Japan*


## Introduction

<p style="text-align:justify;">
We have developed MADGUI, a MAterial Design Graphical User Interface that require no programming knowledge and can be applied to a wide range of fields. This GUI is built using Python and various python libraries including Streamlit, scikit-learn, seaborn, xgboost and more importantly GpyOpt for the Bayesian Optimisation (BO) part. BO is a probability model that find the minimum/maximum of a black-box function (objective function) using a prior function based only on the data collected and performing multiple iterations. The goal of MADGUI is to help researchers to reach the optimum parameters in their research. 
</p>

The following parts are the explanation of how to use the GUI.
<p align="center">
<img src="https://user-images.githubusercontent.com/108456770/223059434-bfa07661-1519-4b48-8a49-3d65c8e5623d.png" alt= “flowchart” width="800" height="450" margin:auto;">
</p>

## Data Preparation

Firstly, to use correctly the GUI you need to have a tabular dataset with some specifications. There is some rules to follow:
* Only numerical values
* No empty space
* Format csv or xlsx
* First line must be columns names (features and targets)
* Dataset must be in the first sheet of your file

Here is an exemple of what it must look like:

<img src="https://user-images.githubusercontent.com/108456770/229692238-a396619f-b0ac-4043-8d04-5316cf55c72b.png" alt= “dataset_exemple”>


When your file is prepared, you can use MADGUI by uploading your file via the button in the sidebar:

<img src="https://user-images.githubusercontent.com/108456770/229692818-7cbce704-5174-4334-b260-23dd38fcf9d4.png" alt= “sidebar” width="167" height="459.5">

## Initialisation

<p style="text-align:justify;">
After uploading your data you have to select what columns are features and which one are the target.
/!\ Take note that the columns where the standard deviation is 0 are already take out from the selection because it doesn't help the prediction or optimisation.
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/108456770/229695425-a3304dcb-614c-486a-acdb-e9ae968f6c92.png" alt = "selection_features" width="358.5" height="421" margin:auto;">
</p>

## Simple analysis

After your selection the GUI perform statistical analysis, first is a quick analysis of each columns (mean, min, max, std,...) and second is a correlation graph between each columns :

<p align="center">
<img src="https://user-images.githubusercontent.com/108456770/229703230-bf4f9f3d-1ff6-4d6b-b610-cf4f10327114.png" alt = "quick_analysis" width="553" height="600"> <img src="https://user-images.githubusercontent.com/108456770/229703254-99e79a55-bdfe-4ece-88a3-86c8428c6e33.png" alt = "correlation" width="600" height="600">
</p>

The GUI also allow users to analyse their datas with Pearson's correlation, the Pearson correlation measures the strength of the linear relationship between two variables:

<p align="center">
<img src="https://user-images.githubusercontent.com/108456770/229713726-eaf2009f-21cc-422c-8408-ec142b766477.png" alt = "Pearson" width="600" height="600" margin:auto;">
</p>


We utilize four methods: ElasticNet, RandomForestRegressor, XGBRegressor or HistGradientBoostingRegressor, and two cross-validation methods: LeaveOneOut or K-fold.

![image](https://user-images.githubusercontent.com/108456770/223050037-8596b6bb-5d73-4d86-bed0-88a3eef6fbc7.png)

![image](https://user-images.githubusercontent.com/108456770/223052582-a2dc7cf4-a7f4-4123-9645-4eda6b172718.png)

An important part of the optimization is the limit for features and possibility to apply constraints, the application take both of it in consideration for the optimization.
The last part allow users to use prediction model and Bayesian Optimization at the same time to unbias the data for the initialisation of the Bayesian Optimization.

![image](https://user-images.githubusercontent.com/108456770/223050417-fe3c8d5b-636d-4176-bedd-ede96b9ff371.png)

Here is an explanation of the Bayesian Optimization (source: http://krasserm.github.io/2018/03/21/bayesian-optimization/)

![image](https://user-images.githubusercontent.com/108456770/215394614-fa624138-568c-4951-b6e7-a4e9c3e005e0.png)

