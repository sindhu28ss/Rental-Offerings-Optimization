# Rental-Offerings-Optimization
## Airbnb Analytics: Analyzing Market Trends, Optimizing Rates, Predicting Room Types, and Uncovering Listing Patterns for Strategic Hosting

<p align="center">
  <img src="https://github.com/sindhu28ss/Rental-Offerings-Optimization/blob/main/Airbnb-logo.png" width="250">
</p>

## Project Overview:
This project dives deep into the dynamic Airbnb market, focusing on using advanced analytics to optimize pricing strategies, enhance guest experiences, and increase host profitability. With Airbnb's widespread influence and its complex marketplace, there is a significant need for hosts to strategically align their offerings with market demands. Through detailed data analysis and predictive modeling, this initiative equips Airbnb hosts with critical insights to optimize their pricing, predict popular room types, and uncover listing patterns, thereby enabling them to make informed decisions that improve their hosting effectiveness.

## Data Source:
The analysis is based on the [US Airbnb Open Data](https://www.kaggle.com/datasets/kritikseth/us-airbnb-open-data/code?datasetId=938452&sortBy=commentCount), which includes detailed listings data across multiple cities in the USA.

## Key Research Questions
- How can trends in the short-term rental market be analyzed effectively?
- What strategies can hosts use to establish competitive Airbnb rates?
- Which room types are most preferred according to current hosting strategies?
- What are the emerging patterns in Airbnb listings that can guide strategic decisions?

### Model 1: Price Prediction using Multiple Linear Regression
- **Objective**: Enable hosts to establish competitive and appealing rates for Airbnb listings through strategic pricing models.
- **Outcome Variable:** price.
- **Evaluation Metric:** Root Mean Squared Error (RMSE)

## Variable Importance Analysis:

A Variable Importance plot was generated to evaluate the contribution of different variables, especially city variables, to the prediction task.
Less influential city variables were identified and excluded.

<p align="center">
  <img src="https://github.com/sindhu28ss/Rental-Offerings-Optimization/blob/main/images/variable%20plot.png" width="500">
</p>

## Exhaustive Search and Backward Elimination:

Applied Exhaustive Search and Backward Elimination techniques to streamline the predictors and retain the most significant variables.
This resulted in a Final Model with only 5 predictor variables. Simplifying the Final Model from 34 to 5 variables improves interpretability and practicality for price prediction. This trade-off aligns with prioritizing a model better suited for real-world applications in predicting prices.
- **Predictors:** availability_365, calculated_host_listings_count, minimum_nights, number_of_reviews, room_type_Private room.
- **Performance:** RMSE: 140.14.

### Model 2: Room Type Prediction using Classification Trees
- **Objective**: Discern the most suitable room type for hosts' listings by considering various booking-related parameters.
- **Outcome Variable:** Room_type.
- **Evaluation Metric:** Accuracy

<p align="center">
  <img src="https://github.com/sindhu28ss/Rental-Offerings-Optimization/blob/main/images/Trees.png" width="1000">
</p>


### Model 3: Clustering to Uncover Patterns in Listings
- **Objective**: Employ clustering techniques to segment Airbnb listings, facilitating nuanced market insights and informed decision-making.
- **Methodology**: Applied clustering algorithms to group listings into distinct categories based on shared characteristics.

**Cluster Insights**:
- **Cluster 0**: Review-Dwelling Stays
- **Cluster 1**: Diverse Accommodations Hub
- **Cluster 2**: Extended Stay Options
- **Cluster 3**: Upscale retreats

<p align="center">
  <img src="https://github.com/sindhu28ss/Rental-Offerings-Optimization/blob/main/images/Cluster.png" width="800">
</p>

**Cluster distributions**:
- **Cluster 0**: blue
- **Cluster 1**: green
- **Cluster 2**: red
- **Cluster 3**: orange

<p align="center">
  <img src="https://github.com/sindhu28ss/Rental-Offerings-Optimization/blob/main/images/map.png" width="800">
</p>


## Recommendations to the Host

- **For Diverse Accommodation Hubs**: Encourage customer reviews to enhance visibility and reputation. Stand out by actively requesting feedback from guests to improve and highlight your listing’s unique aspects.

- **For Upscale Retreats**: Offer personalized experiences that prompt guests to leave positive reviews. Consider exclusive amenities or tailored services that align with the expectations of guests seeking luxury accommodations.

- **For Extended Stay Properties**: Highlight and promote the amenities that are most attractive to long-term guests. Ensure that these features are prominently mentioned in your listing to attract guests looking for extended stays.

- **Competitive Pricing Strategies**: Maintain year-round availability to maximize booking potential. For properties with private rooms, consider setting prices slightly lower than other room types to increase occupancy rates. This strategy can be particularly effective in markets with high competition for private rooms.

- **Special Considerations for New York**: In markets like New York where demand can support higher rates, price private rooms between $65.5 and $85.5. This pricing strategy aligns with guest willingness to pay more due to the location’s desirability.

**Ongoing Strategy Adjustments**: Regularly evaluate and adjust your pricing strategies based on the latest market trends and guest feedback. This dynamic approach ensures that your property remains competitive and appealing, maximizing both occupancy and revenue.





