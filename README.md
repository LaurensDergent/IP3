IP 3: Predicting production and attraction of zones based on POI's and population density with an xgBoost model.
Description of the project

The aim of this project is to predict the production and the attraction per zone by using a machine learning model. The data used for this is the information from the Point Of Interest (POIs)[ ] and the density per zone. The POIs for the studied area were made available through Lotte Notelaers and the densities per zone have been calculated using the public available data of the number of inhabitants per ha in Flanders[ ]. As actual values, the production and the attraction calculated according to the department Mobiliteit & Openbare Werken (MOW) are assumed.
An XGboost model is used as the machine learning model since it is a widely used model in the literature. SHAP values are used to interpret the results of the model. To evaluate the performance of the model, it is compared with the linear model of the paper of Notelaers, L. et al. [1]
Research questions

Four models will be made to help answer the research questions. A small model will be trained on the data of Antwerp. A full model will be trained on the zones of Antwerp and smaller cities such as Mechelen. These two models will be used to predict the production and attraction of the zones.
The main goal is to create a model that is reliable and gives decent results. The following research questions are examined using this model:
1)	Does a machine learning model provide better estimates than a linear model?
2)	How does the full model perform on different sizes of cities?
3)	How does the small model perform on  smaller cities?
4)	Is it useful to add additional data from smaller cities to predict a larger city?
 
Files
Overview files:
The files for this project are as follows:
•	SHAP.ipynb: Explanation and background information on SHAP values
•	density_per_zone.ipynb: File to compute the density per zone
•	combine_data.ipynb: File that creates the dataset for the models. It combines the data of MOW, POIs and the density per zone to one dataset.
•	4 Models: 
o	Full_model_attraction.ipynb: Model to predict the attraction based on training data of multiple cities
o	Full_model_production.ipynb: Model to predict the production based on training data of multiple cities
o	Small_model_attraction.ipynb: Model to predict the attraction based on training data of Antwerpen
o	Small_model_attraction.ipynb: Model to predict the production based on training data of Antwerpen


Reading files
The following order is recommended to read the files:
1)	SHAP.ipynb: If desired, read first the background information on SHAP values
Note: This is the information already presented in March
2)	density_per_zone.ipynb : If desired, read the file to calculate the density per zone
Note: Not essential as this also comes back briefly in the presentation and this is not necessary for understanding the rest of the project
3)	combine_data.ipynb: If desired, read the file that creates the dataset for the model
Note: This file contains no insights. 
This file does the following:
•	Calculates production and attraction per zone using the data from MOW
•	Calculates totals per zone of the POIs' categories by using the POIs
•	Creates one large dataset combining the information of the density, the production and attraction and the POIs of the zones of interest
4)	Models: 
It is recommended to read the full models first. These files are fully commented and contain all the descriptions. The small models have the same comments as the full models. However no elaborate descriptions are added as the small models serve as support to answer the research questionss. Moreover, it is also recommended to read the attraction model first and then the production model, as the production model contains some comparisons with the attraction model. In summary, the recommended order is:
•	Full_model_attraction.ipynb
•	Full_model_production.ipynb
•	Small_model_attraction.ipynb
•	Small_model_attraction.ipynb
