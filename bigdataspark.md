---
layout: archive-dates
permalink: /bigdataspark/
title: Big Data Applications
---

-------------

## Spark in Databricks

This project uses Spark in Databricks to forecast the energy production of wind turbines located at Sotavento, Spain. The study uses ML models to predict the electricity generation six hours ahead, based on wind forecast data.

- [PySpark Applications in Databricks](/Notebooks/energy-prediction-pyspark.html)

Since weather patterns are complex and vary greatly, I explore the following 3 questions that could significantly influence the performance of the predictive models:

1. **Localized Data**: Is it enough to use meteorological inputs only from location 13? This would mean determining whether this localized data/information can actually encapsulate the necessary information to forecast energy production accurately.

2. **Feature Engineering and Inclusion of Wind Vector Modulus**: To enhance the model's predictive capabilities, I consider the addition of the wind vector modulus at a height of 100 meters, calculated as the square root of the sum of the squared components of the wind vector (u100 and v100). This will tell me if integrating this aerodynamic parameter can refine my predictions by accounting for the wind's magnitude and directionality.

3. **Comparative Error Analysis**: Of course lastly, I perform a comparative analysis of the Mean Absolute Error (MAE) across different model iterations which should seeks to evaluate whether using only the most influential 25%, 50%, or 75% of input variables will create a model robust enough to predict Sotavento's energy production with newly available forecast data.
