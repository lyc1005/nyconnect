# nyconnect
#### [Wesley Chioh](https://github.com/westerleyy), [Erik Lopez](https://github.com/lobodemonte), [Ziyu Yan](https://github.com/ZiyuYan9), [Yichen Liu](https://github.com/lyc1005)  
#### Supported by: 
#### Zachary Gold @ Department of Information Technology and Telecommunications 
#### Junaid Khan @ NYU Center for Urban Science + Progress
---

#### Overview

The Covid-19 pandemic has revealed the existential importance of internet connectivity in our modern daily lives. However, internet is not magic. It does not exist in a vacuum. As consumers, we are connected to the internet by Internet Service Providers such as Verizon, and Charter, just to name a few. Like any other economic activity, it is regulated by the city government. However, just because its ubiquity is not synonymous with universality. More than 1.5 million New Yorkers, or approximately 18%, do not have any high-speed internet connection.  

Hence, there are a few questions to be answered:  
* Is there an optimal number of Internet Service Providers for the New York City urban broadband market in achieving the goal of universal broadband access?
* What can the government do to achieve universal broadband access?  
* How can broadband affordability be measured and determined?

To answer these questions, the team looked into service provision data from the Federal Communications Commission, demographic surveys from the Census Bureau, geographic boundaries from the New York City government, pricing data scraped by DoITT, and consumer tweets. The data processing and analytical methods include:
* Geoprocessing in QGIS and Python
* Spatial Autocorrelation
* Spatial Regression
* KMeans Clustering
* Bayesian Network
* Text Mining and Sentiment Analysis
  
Fundamentally, there is a price-floor to how low broadband plans can cost in the free market given how much capital investment is needed in the first place. Increased competition can only do so much to bring the costs down. Instead, the results of this project point towards a policy framework that focuses on subsidizing access for the most needy. Income is the most significant variable in determining a household's decision to subscribe to broadband access, not the number of providers.

---

#### Repo Structure

This repository is split into two main folders. `data` contains the datasets used. `analysis` is where Jupyter notebooks with the analyses sit.  

`data`:
* 2010_Census_Blocks:  Shapefile of NYC's Census Blocks as designated by Census Bureau from the 2010 Decennial Census.
* 2010_Census_Tracts:  Shapefile of NYC's Census Tracts as designated by Census Bureau from the 2010 Decennial Census.
* ACS_Internet_Subscription: American Community Survey (ACS) 2017 & 2018 tables B28002 and S2801 showing household internet subscription at different geographical scales in NYC.
* Broadband Prices: Broadband pricing data in NYC provided by DoITT.
* Cellular_Towers: NYC Department of Buildings and Federal Communications Commission (FCC) data on rooftop cellular tower installations.
* Demographics: ACS 2010-2018 table B01001 with demographic information (age, sex, income, basic count) of NYC's Census Tracts.
* FCC_477: FCC Form 477 2017-2019 detailing internet service provision per census block
* Internet_Master_Plan_Adoption: NYC Mayor's Office of the Chief Technology Officer report on key indicators of broadband adoption, service and infrastructure in NYC.
* NTAs: SHapefile of NYC's Neighborhood Tabulation Areas and Census Tracts Equivalence Tables
* Others: Peripheral datasets obtained but not used.  

`analysis`:  
* Bayes_Network_Analysis.ipynb: Bayes Network identifying causal relationships between demographic variables and household internet subscription rates
* Broadband Data Analysis.ipynb: Exploratory Data Analysis of Internet Master Plan and FCC Form 477 2019
* Demographics_KMeans.ipynb: KMeans Clustering of demographic and business-related datasets
* FCC_Form_477_Provider_Analysis.ipynb: Analysis and processing of FCC 477 data
* NTA_level_regression.ipynb: Regression analysis of broadband pricing and ISPs at geographical scale of NTAs 
* Price_Data_Visualization.ipynb: Visualizing changes in broadband pricing over time
* Regression_Analysis.ipynb: Regression analysis of broadband pricing and ISPs at geographical scale of Census Tracts
* Reprojection.qgz: Reprojection of shapefiles to common projection using QGIS
* Subscription_Autocorrelation_SpatReg.ipynb: Testing for Spatial Autocorrelation, (Local & Global) Moran's I, Spatial Regression of subscription and demographic data  
* Twitter analysis.ipynb: Analysis of tweets scraped 
* Twitter Scraper.ipynb: Twitter scraping tool
* wifi_hotspots_analysis.ipynb: Analysis of wifi and hotspots in NYC
