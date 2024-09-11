## Dataset Content
* The dataset is sourced from [Kaggle](https://www.kaggle.com/codeinstitute/housing-prices-data). We created a user story in which data analytics can be applied in a real project in the workplace. 
* The dataset has almost 1.5 thousand rows and represents housing records from Ames, Iowa. It indicates the house profile (Floor Area, Basement, Garage, Kitchen, Lot, Porch, Wood Deck, Year Built) and its respective sale price for houses built between 1872 and 2010.

|Variable|Meaning|Units|
|:----|:----|:----|
|1stFlrSF|First Floor square feet|334 - 4692|
|2ndFlrSF|Second-floor square feet|0 - 2065|
|BedroomAbvGr|Bedrooms above grade (does NOT include basement bedrooms)|0 - 8|
|BsmtExposure|Refers to walkout or garden level walls|Gd: Good Exposure; Av: Average Exposure; Mn: Minimum Exposure; No: No Exposure; None: No Basement|
|BsmtFinType1|Rating of basement finished area|GLQ: Good Living Quarters; ALQ: Average Living Quarters; BLQ: Below Average Living Quarters; Rec: Average Rec Room; LwQ: Low Quality; Unf: Unfinshed; None: No Basement|
|BsmtFinSF1|Type 1 finished square feet|0 - 5644|
|BsmtUnfSF|Unfinished square feet of basement area|0 - 2336|
|TotalBsmtSF|Total square feet of basement area|0 - 6110|
|GarageArea|Size of garage in square feet|0 - 1418|
|GarageFinish|Interior finish of the garage|Fin: Finished; RFn: Rough Finished; Unf: Unfinished; None: No Garage|
|GarageYrBlt|Year garage was built|1900 - 2010|
|GrLivArea|Above grade (ground) living area square feet|334 - 5642|
|KitchenQual|Kitchen quality|Ex: Excellent; Gd: Good; TA: Typical/Average; Fa: Fair; Po: Poor|
|LotArea| Lot size in square feet|1300 - 215245|
|LotFrontage| Linear feet of street connected to property|21 - 313|
|MasVnrArea|Masonry veneer area in square feet|0 - 1600|
|EnclosedPorch|Enclosed porch area in square feet|0 - 286|
|OpenPorchSF|Open porch area in square feet|0 - 547|
|OverallCond|Rates the overall condition of the house|10: Very Excellent; 9: Excellent; 8: Very Good; 7: Good; 6: Above Average; 5: Average; 4: Below Average; 3: Fair; 2: Poor; 1: Very Poor|
|OverallQual|Rates the overall material and finish of the house|10: Very Excellent; 9: Excellent; 8: Very Good; 7: Good; 6: Above Average; 5: Average; 4: Below Average; 3: Fair; 2: Poor; 1: Very Poor|
|WoodDeckSF|Wood deck area in square feet|0 - 736|
|YearBuilt|Original construction date|1872 - 2010|
|YearRemodAdd|Remodel date (same as construction date if no remodelling or additions)|1950 - 2010|
|SalePrice|Sale Price|34900 - 755000|





## Business Requirements
As a data analyst, your friend, who has received an inheritance from a deceased great-grandfather in Ames, Iowa, has asked you to help maximise the sales price for the inherited properties.

Although your friend has an excellent understanding of property prices in her own state and residential area, she fears that basing her estimates for property worth on her current knowledge might lead to inaccurate appraisals. What makes a house desirable and valuable where she comes from might not be the same in Ames, Iowa. She found a public dataset with house prices for Ames, Iowa, and will provide you with that.

* 1—The client is interested in discovering how the house attributes correlate with the sale price. Therefore, the client expects data visualisations of the correlated variables against the sale price to show this.
* 2—The client is interested in predicting the sales price of her four inherited houses and any other house in Ames, Iowa.


## Hypothesis and how to validate?
* Using my prior housing knowledge, here are my  hypothesis(es) : 
* 1: We suspect that not all features will be used to predict the sale price. Only a few sets of features will be relevant. 
	* How to validate: When using conventional ML, the feature selection step will tell you which features are more relevant to use in conjunction to predict the sale price.
* 2: We suspect higher sale price levels happen with houses that were built after 1980. 
	* How to validate: We will create an additional column in the dataset indicating whether the house was built before or after 1980. Then, we will conduct a statistical test to compare sale price levels between the 2 groups.
* 3: The 4 inherited houses have OverallQual levels of 5 and 6. We suspect that the sale price level from houses with OverallQuall 6 is statistically higher than OverallQuall  5. 
	* How to validate: we will conduct a statistical test to compare levels between the 2 groups.




## The rationale to map the business requirements to the Data Visualisations 
* **Business Requirement 1:** Data Visualisation and Correlation study
	* As a client, I want to inspect the data related to the house records so that I can discover how the house attributes correlate with the sale price.
	* As a client, I want to conduct a correlation study (Pearson and Spearman) to understand better how the variables are correlated to the Sale Price so that I can discover how the house attributes correlate with the sale price.
	* As a client, I want to plot the main variables against the Sale Price to visualise insights and discover how the house attributes correlate with the sale price.


## Dashboard Design
### Page 1: Quick project summary
* Quick project summary
	* "General Information" or "Project Terms & Jargon"
	* Project Dataset Description
	* Link to additional information
	* State Business requirements


### Page 2: House Sale Price UI
* State business requirement 2
* A table displaying the four inherited houses' attributes and their respective predicted sale price
* A paragraph with the summed predicted price for all 4 inherited houses
* Set of widgets inputs, which relates to the house profile used to predict the sale price.
* "Predict House Sale Price" button that serves the house profile data to our ML pipeline and renders the predicted sale price. 

### Page 4: Project Hypothesis and Validation
* Block for each project hypothesis. Describe the conclusion and how you validated it.

## Unfixed Bugs
* No bugs to report

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. At the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly in case all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.


## Main Data Analysis and Libraries
* Numpy and Pandas are used for data manipulation in the jupyter notebooks
* Matplotlib and Seaborn display scatter plots, line plots, or bar plots.
* Pandas Profiling is used to generate Quick EDA reports in the jupyter notebooks
* Plotly is used to display an interactive Parallel Plot on the Sale Price Study page.
* Ppscore is used in Jupyter Notebooks to understand better how the features and target interact with each other
* Streamlit is used as a dashboard tool
* feature-engine is used for feature engineering for tasks present in the ML pipeline such as DropFeatures, MeanMedianImputer, CategoricalImputer

## Credits 

* In this section, you need to reference where you got your content, media, and extra help. While it is common practice to use code from other repositories and tutorials, it is essential to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 


## Acknowledgements (optional)
* I would like to thank the following people who provided support through this project.
