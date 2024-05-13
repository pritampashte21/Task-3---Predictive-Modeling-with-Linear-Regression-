In this project we'll use condominium sales data from all 5 boroughs of New York City to determine how well the size of a condominium (measured in gross square feet) explains/predicts sale price for each individual borough 
& across New York City as a whole. 
This property sales data is publicly available here (https://data.world/dataquest/nyc-property-sales-data) and covers sales records from a twelve-month period (from November 1, 2018, through October 31, 2019).
(refer to file named NYC_property_sale_prices_guided).
The goal of the project is to: 
- apply our skills particularly linear regression models (aka bivariate linear regression),
- evaluate summaries of regression statistics and
- assess the model quality
- test hypothesis
- use functions in the `broom` package that allow us to nest, tidy, augment, & unnest data

The modeling was done using data for February,2023 - January,2024 as well. (refer to file named predicting_NYC_property_sale_prices).
We plotted sale price against property size for NYC as a whole & for each borough individually as below
![Untitled](https://github.com/Benazir023/Predicting_NYC_property_sale_prices/assets/123881327/ee541343-a34a-4be2-a60b-4e90f819c590)

![Untitled](https://github.com/Benazir023/Predicting_NYC_property_sale_prices/assets/123881327/a73d97ec-7a87-420a-90a1-c331e695e6c1)

Regression summary statistics are available for both NYC & each borough. These statistics include the coefficients shown in the following image (refer to file named output)
![image](https://github.com/Benazir023/Predicting_NYC_property_sale_prices/assets/123881327/814b0fbf-387b-4c13-a680-76955d6fa743)

For instance the equation for sale price in Bronx whould be written as <br>
_sale_price = 0.0000254 + 649 * gross_square_feet_

Our analysis showed that, in general, the gross_square_feet variable is useful for explaining, or estimating, sale_price for property sales in New York City. 
We observed that removing multi-unit sales from the dataset increased model accuracy, from 31.77% to 61.66%. However, there is still room for improvement. 
With linear models generated for New York City as a whole, and with linear models generated for each borough individually, we observed in all cases that the t-statistic was high enough, and the p-value was low enough, 
to declare that there is a relationship between gross_square_feet and sale_price.

Regression summary statistics indicate that gross_square_feet is a better single predictor of sale_price in some boroughs versus others. 
For instance, the R-squared value was estimated at approximately 0.34 and 0.48 in Queens and Staten Island compared to an estimate of 0.63 in Manhattan. 
These differences in R-squared correspond with the scatterplots generated for each borough; the strength of sale prices versus gross square feet was higher, and the dispersion (spread), was lower for Manhattan compared to Queens 
where the relationship was moderate because the data was more spread out.

