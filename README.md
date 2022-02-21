# List Price Analysis

![map](images/KC_simplemap_Oct2013.jpg)

## Business Problem

The King County Realty Team wants to focus on setting a more accurate list price for their seller clients. This analysis has given the real estate agency a way to set a list price based on data for specific characteristics: grade, view, living sqft, yr built, and floors. These characteristics were chosen based on using data that best fits the regression model to insure the model would compute the best results with minimal error. The goal is, this information will allow the agents to give their clients a more legitimate estimate on the value of their home.

## The Data

The data used for this project was from the King Country Dataset, a dataset of real real-estate data from King County Washington. The data frame is called "kc_house_data" and it contains 21597 rows and 21 columns. The columns used in this analysis were `price`, `bedrooms`, `bathrooms`, `sqft_living`, `sqft_lot`, `floors`, `waterfront`, `view`, `condition`, `grade`, `sqft_above`, `sqft_basement`, `yr_built`, `yr_renovated`, `basement_yes_no`, `yr_renovated_ob`. With 'price' being the target variable. Each of the 21597 rows represents a house sold in the county.

## Methods

This project used the King County housing data to make a regression model. The coefficients from this model was used to find the associated dollar amount for the different features. 

The data was cleaned, scrubbed, and explored by removing multicollinearity, removing outliers, scaling the data, accounting for categorical data, and removing data that was heteroscedastic. 
 

## Results

The final model had an R-square value of 0.615 which can be described as: 61.5% of the variations in the dependent variable 'price' are explained by the independent variables in our model. A higher R squared value means there is a less chance of error. The remaining percentage (in this model ~ 39%) represents the variance explained by error, the part that the model failed to grasp. This R-square value is relatively low and would need to be raised to use the model for its intended purposes

The coeffients in this model allow for adjustment on the price be made, for example:
    
   -The model for 'sqft_living' has a coefficient of 111. This is interpeted by saying each unit of sqft living changes the price by 111 dollars. So taking the known sqft of living space in the house and multipling it by 111 will lead to price estimate to account for the sqft living. For example if a house had 1,500 sqft living, the calculation would be 1,500 x 111 which would tell us to add 166,500 dollars to the price.
   
   -The model for 'view_EXCELLENT' has a coefficient of 178,710. This is a categorical variable and so this is interpeted as if the house has that characteristic then add 178,710 dollars to the price.

The same process would be followed for year built, number of floors, and view. Once all price values are found they would be added together to get a list price estimate. 

## Conclusion

Interpretion of the regression model led to the following findings:
    
- The coefficients for the respective grade, view, year built, and sqft of living space of the home can be used to adequately adjust the list price.
- The final model had an R-square value of 0.615 this model should be strictly used alongside with personal judgement of the agents.

While this model can be used to help real estate agents come up with a predicted list price for their clients, the model does not have high confidence that the independent variables actually explain the variation in price. This model should be further improved and if it is used in its current state, it should be used with caution 

## Next Steps

Evaluate the change on the model that happens when adjusting methods for:
- Normalizing/transforming data differently 
- Dealing with categorical data ex: Assigning blank data in categorical variables differently
- Detect outliers differently

Lastly, the location data that was removed in the being of the model could be found useful if used correctly 

## For More Information

See the full analysis here: [Jupyter Notebook](./List_Price_Analysis.ipynb) or review the presentation: [presentation](./List_Price_Presentation.pdf).

## Repository Structure

```
├── data
├── images
├── List_Price_Analysis.ipynb
├── List_Price_Presentation.pdf
└── README.md
```


