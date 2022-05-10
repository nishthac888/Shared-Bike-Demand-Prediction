# Bike-Sharing-Assignment-Linear-Regression

A bike-sharing system is a service that makes bikes accessible for shared use to individuals for a fee or for free on a short-term basis.
Many bike sharing systems let users rent a bike from a "dock," which is generally computer-controlled and where the user inputs payment information and the system unlocks the bike.
After that, the bike can be returned to another dock in the same system. 

BoomBikes, a US bike-sharing company, has lately seen a significant drop in sales because to the ongoing Corona outbreak.
In the present market environment, the firm is struggling to stay afloat.
As a result, it has decided to develop a thoughtful business strategy in order to increase income as soon as the current lockdown ends and the economy returns to normal. 

BoomBikes hopes to have a better understanding of people's desire for shared bikes when the current Covid-19-related quarantine expires across the country.
They planned this to position themselves to meet people's demands whenever the situation improves all around, to differentiate themselves from other service providers, and to profit handsomely. 

They hired a consulting firm to help them figure out what factors influence demand for these shared bikes.
They want to know what variables are influencing demand for these shared bikes in the American market.
The firm is curious about the following:

What factors play a role in projecting demand for shared bikes?
How closely those factors accurately characterise the bike's requirements
The service provider organisation has amassed a vast dataset on daily bike demands across the American market based on several parameters based on numerous weather studies and people's styles.

Business Objective: Using the supplied independent variables, predict the demand for shared bikes.
The management will utilise it to figure out how the needs alter depending on the characteristics.
They may adjust their company plan properly to match demand levels and client expectations.
Furthermore, the model will assist management in comprehending the demand dynamics of a new market. 

Data Preparation:
You can see in the dataset that some variables, such as 'weathersit' and'season,' have values of 1, 2, 3, 4, which correspond to specific labels (as can be seen in the data dictionary).
These numerical numbers connected with the labels may give the impression that they are in some sort of order, but this is not the case .
Before starting with model construction, it is advisable to transform such feature data into categorical string values.
To better comprehend all of the independent variables, please see the data dictionary.  

You'll see that the column 'yr' has two values of 0 and 1, denoting the years 2018 and 2019.
You could assume that dropping this column is a smart idea because it just has two values and so isn't a value-add to the model.
However, as these bike-sharing systems are steadily gaining popularity, demand for these bikes is growing year after year, indicating that the column 'yr' might be a useful variable for forecasting.
So think again before you throw it out. 

Model Building

There are three columns titled 'casual,"registered,' and 'cnt' in the dataset supplied.
The 'casual' variable displays the amount of casual users who have rented anything.
On the other hand, the variable'registered' displays the total number of registered users who have placed a booking on a given day.
Finally, the 'cnt' variable shows the total number of bike rentals, which includes both casual and registered rentals.
This 'cnt' should be used as the target variable in the model. 

Model Evaluation:
When you're finished with model construction and residual analysis, and you've made predictions on the test set, use the following two lines of code to compute the R-squared score on the test set.

from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
 