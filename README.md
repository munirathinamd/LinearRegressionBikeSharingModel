# Linear Regression - Bike Sharing System
> A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

> A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 


## Table of Contents
* [Business Overview](#Business-Overview)
* [Business Goal](#Business-Goal)
* [Technologies Used](#technologies-used)
* [Steps Followed](#Steps-Followed)
* [Analysis Results](#Analysis-Results)
* [Conclusions](#conclusions)


<!-- You can include any other section that is pertinent to your problem -->

## Business Overview
BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.

They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

-   Which variables are significant in predicting the demand for shared bikes.
-   How well those variables describe the bike demands


## Business Goal
I require to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 


## Technologies Used
-   Numpy Version: 1.20.3
-   Pandas Version: 1.3.4
-   Matplotlib Version: 3.4.3
-   Seaborn Version: 0.11.2
-   The scikit-learn Version: 0.24.2.
-   The statsmodels Version: 0.12.2.

## Steps Followed
> ### Exploratory Data Analysis
    - Data Cleaning 
    - Missing Data Treatment
    - Remove Irrelevant Variables wrt both data and business use cases
    - Outliers Analysis and Treatments
    - Deriving Categorial columns
    - Univariate Analysis
    - Bivariate Analysis
    - Multivariate Analysis

> ### Model Preparation
    - Training and Test data split
    - Feature Scaling - StandardScaler
    - Feature Engineering & Selection using RFE and Variance Inflation factor
    - Model preparation
    - Residual Analysis
    - Model Evaluation & Assessment
    - Prediction
    - Conclusion & Analysis

## Analysis Results
>   ### Exploratory Data Analysis
    -   62.33 % of total Bike hired in year 2019
    -   Around 97.62% of bike hiring is on non holidays
    -   Around 69.6% of bike hiring is on working days
    -   Around 29.58% of bike hiring happened in the temp between 25-30
    -   Around 26.97% of bike hiring happened in the actual temp between 25-30
    -   There is a vast different in actual temperature and temperature variable . Especially, in slab of 30-35, actual is of 25.3% whereas temp is of 11.69%
    -   Around 64.5%of bike hiring happened in the humidity between 50 and 75
    -   Around 37%of bike hiring happened in the wind speed between 10 and 15. Also, good % of bike hiring happened for the wind speed is between 5 to 25
    -   Highest number of bike hiring is in fall and then summer seasons
    -   Around 69% of total bike hiring is in clear / partial cloudy weather and then 30.24% in the mist weather. If it’s raining, the bike hiring is almost not happening.
    -   More number of bike hiring happened between May and Oct (between ~32K & ~35K). In which Aug month has high.
    -   Cnt variable is correlated with temp (high corr), atemp(high corr), yr(high corr), season, mnth, windspeed. Only wind speed is negative correlation
    -   There is a linear relationship between cnt and temp; cnt and atemp varaibles
    -   temp variable have high correlation with atemp variable
    -   mnth & season have good correlation

>   ### Model Analysis
    -   Year: With 2 years data, we can say a unit increase in year variable, the bike hire increases by 0.2416 units
    -   Temperature: A unit crease in temperature, bike hire increases by 0.45960 units
    -   Months: In the month of September, bike hire increases by 0.0528 units whereas in Jul, bike hire decreases by 0.0647 units
    -   Season: In winter season, bike hire increases by 0.0495 units whereas in spring season, bike hire decreases by 0.1474 units
    -   Weathersit: In weathersit-2(Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist), the bike hire decreases by 0.0794 units. In weathersit-3 (Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds), the bike hire decreases by 0.2610 units
    -   Wind Speed: For a unit increase in wind speed, bike hire decreases by 0.0914 units

>   ### Equation best fitted surface for the final model is
    cnt=0.2147+ yr(0.2416)+temp (0.45960) -mnth_jul(0.0647) +mnth_sept(0.0528) -season_spring(0.1474) +season_winter (0.0495) -weathersit_mist(0.0794) - weathersit_light_rain(0.2610) - windspeed(0.0914)

>   ### Significant Features
    Below are the significant features considering both model analysis and EDA
    -   Year
    -   Temperature
    -   Month-Aug,Sep,Jul
    -   Weathersit_mist
    -   Season- Spring and Winter
    -   Wind Speed
    -   Humidity
    -   Holiday
    -   Workingday

## Conclusions
    With the given data set, created a model to predict the demand for bike sharing. I also performed EDA to understand each variable's significance and its correlation with other variables. Finally, we provided model analysis results and also listed the significant variables used for demand predictions.


## Contact
Created by [@munirathinamd] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->