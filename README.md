# MADGUI : Material Design Graphical User Interface
User-friendly Graphical User Interface (GUI) developed at the National Institute for Materials Science (NIMS, MaDIS) for performing statistical data analysis, machine learning (ML) modelisation, and composition/process optimisation through Bayesian optimisation.

Can be used directly without any installation with the link below:
(add link when app deployed)

Developers:

Christophe BAJAN* & Guillaume LAMBARD*

*National Institute for Materials Science, Tsukuba, Japan

Test 

![image](https://user-images.githubusercontent.com/108456770/223058862-103e3b37-b694-4d5f-87c9-d8b92e9b8a5c.png)

The application allow users to analyse their datas (with Pearson's correlation for example)
We utilize four methods: ElasticNet, RandomForestRegressor, XGBRegressor or HistGradientBoostingRegressor, and two cross-validation methods: LeaveOneOut or K-fold.

![image](https://user-images.githubusercontent.com/108456770/223050037-8596b6bb-5d73-4d86-bed0-88a3eef6fbc7.png)

![image](https://user-images.githubusercontent.com/108456770/223052582-a2dc7cf4-a7f4-4123-9645-4eda6b172718.png)

An important part of the optimization is the limit for the features and the constraints, the application take both of it in consideration for the optimization.
The last part allow users to use prediction model and Bayesian Optimization at the same time to unbias the data for the initialisation of the Bayesian Optimization.

![image](https://user-images.githubusercontent.com/108456770/223050417-fe3c8d5b-636d-4176-bedd-ede96b9ff371.png)

Here is an explanation of the Bayesian Optimization (source: http://krasserm.github.io/2018/03/21/bayesian-optimization/)

![image](https://user-images.githubusercontent.com/108456770/215394614-fa624138-568c-4951-b6e7-a4e9c3e005e0.png)

