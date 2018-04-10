# Capstone

Technical Report

Introduction 
According to the USDA, food deserts are defined as parts of the country vapid of fresh fruit, vegetables, and other healthful whole foods, usually found in impoverished areas.  Posted on their website is a data visualization of a map of the U.S. which gives a different color gradient concentration of census tracts based on the distance of a population from a supermarket and not having access to a vehicle.

Summary of Primary Data Set
The current version of the Food Environment Atlas has over 275 variables, including new indicators on access and proximity to a grocery store for sub populations; an indicator on the SNAP Combined Application Project for recipients of Supplemental Security Income (at the state level); and indicators on farmers' markets that report accepting credit cards or report selling baked and prepared food products. All of the data included in the Atlas are aggregated into an Excel spreadsheet for easy download. Note: the information listed is by county.

Problem Statements 
What other factors beside a population’s distance to a grocery market can determine if a county will have a higher concentration of food deserts? Would it be possible to create a model to identify counties that are more likely to contain food deserts?

Data Method
The 275 variables was reduced to 54 variables for the project's dataset. Our y-variable is 'Low Access: All Populations (%)', which is the percentage of the population that lives one mile away from a grocery store in an urban area and 10 miles away if they live in a rural area.

Variables were chosen and placed in the following categories:
Low Access (Race): Low access population percentages for different races
Stores: Type of stores
Restaurants: Food service type and expenditures
Assistance: Types of food assistance programs provided
Sales Tax: Taxes of various food items
Local Food Operations: Types of local food operations present e.g. farmers' markets 
Health: Health status of residents
Socioeconomic: Racial and economic status of all residents (regardless of being low access or not) 


Modeling
The following models are used for analysis:

1. Decision Tree Regression: As the y-variable is 'Low Access: All Populations (%)', all variables related to this e.g. 'Low Access: Asian Population' were dropped out as this would strongly impact our y-variable. After running a features importance analysis, we can determine which variables are most impactful in this model.

2. Logistic Regression, KNN (with various clusters sizes), Random Forest Models: The 'Low Access: All Populations (%)' variable is set to a binary column with values of 'high' vs 'low'. If a county's low access percentage is less than the median of all counties, it's set as 'low'. If not, it's set as 'high' (and 'high' means the county is more likely to have food deserts) Once again, without using the low access variables tied to race, all other variables will be used in modeling.