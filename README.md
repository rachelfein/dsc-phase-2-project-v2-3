# List Price Analysis



## Business Problem

My stakeholder is King County Reality Team, who wants to focus on setting a more accurate list price for their seller clients. This analysis has given the real estate agency a way to set a list price based on data for specific characteristics: view, floors, condition, sqft. These characteristics were choosen based on using data that best fits the linear model to insure the model would compute the best results with minamal error. The goal is this information will allow the agents to give their clients a more legitimate estimate on the value of their home.

## The Data

The data used for this project was from the King Country Dataset, a dataset of real real-estate data from King County Washington. The data frame is called "kc_house_data" and it contains 21597 rows and 21 columns. The columns used in this analysis were `price`, `bedrooms`, `bathrooms`, `sqft_living`, `sqft_lot`, `floors`, `waterfront`, `view`, `condition`, `grade`, `sqft_above`, `sqft_basement`, `yr_built`, `yr_renovated`, `basement_yes_no`, `yr_renovated_ob`. With 'price' being the target variable. Each of the 21597 rows represents a house sold in the county.

## Methods

This project used the King County housing data to make a regression model. The model was used to find a baseline price for a home and find the associated dollar amount for the features. 

The data was cleaned, scrubed, and explored by removing multicolinarity, removing outliers, scaling the data, and removing data that was heteroscedastic. 

## Results

The final model had an R-square value of 0.615 which can be described as: 61.5% of the variations in the dependent variable 'price' are explained by the independent variables in our model. A higher R squared value means there is a less chance of error. The remaining percentage (in this model ~ 39%) represents the variance explained by error, the part that the model failed to grasp. This R-square value is relatively low and would need to be raised to use the model for its intended purposes

The coeffients in this model allow for adjustment on the base price be made, two examples are:
    
   -  The coefficient for 'grade_7_average' has a coefficient of -387,936 since this is categorical data, this would be interpreted as if true, it would lower the price of the home by 387,936 dollars from the base price of 858,720 dollars which is intercept value found in the model. 
   -  The coefficient for 'view_EXCELLENT' has a coefficient of 178,710 since this is categorical data, this would be interpreted as if true, it would raise the price of the home by 178,710 dollars from the base price of 858,720 dollars which is intercept value found in the model.

## Conclusion

Interpretion of the regression model led to the following findings:
    
- The coefficients for the respective grade, view, year built, and sqft of living space of the home can be used to adequately adjust the list price
- The final model had an R-square value of 0.615 this model should be strictly used alongside with personal judgement of the agents.

## Next Steps

Evaluate the change on the model that happens when adjusting methods for:
- Normalizing/transforming data differently 
- Assigning blank data in categorical variables differently
- Detect outliers differently

Lastly, the location data that was removed in the being of the model could be found useful if used correctly 

## For More Information

See the full analysis here: [Jupyter Notebook](./Microsoft-Movie-Recommendations.ipynb) or review the presentation: [presentation](./Microsoft_Movie_Presentation.pdf).

## Repository Structure

```
├── data
├── images
├── list_price_analysis.ipynb
├── Project_Presentation.pdf
└── README.md
```


