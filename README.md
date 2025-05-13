**How Citi Bike Meets Demand**

**Overview**

This project aims to optimize Citi Bike allocations across stations in New York City using regression and optimization models. By analyzing usage data, we recommend how to distribute a fixed number of bikes to maximize trips and meet demand efficiently.

**Objective**

Determine the number of bikes to stock at each station to maximize daily trips.

**Key Questions**

• What is the distribution of weekday vs. evening trips?

• How many bikes should be allocated to each selected station?

**Dataset**

Total records: 859,294

Missing values: 10,681 (1.22%)

Key variables include:

Start/End Station IDs

Trip Duration

Distance (miles)

Start Per Capita Income

Percentage of Households Without Vehicles

Time of Day (Day/Evening)

**Descriptive Analytics**

90.25% of riders are subscribers, indicating weekday commute use.

Mean demand: 45.37 bikes (SD: 32.53)

Mean trip duration: 12.97 minutes

Most demand occurs in East Village and Lower East Side during the evening.

**Predictive Analytics**

Linear regression used to model bike demand

Model R² = 0.363 (36.3% of variance explained)

**Key Predictors**

• Time of Day

• Station locations

• Per capita income and car ownership

• Trip duration and distance

**Regression Equation**

Demand = -60.01 - 0.0052*StartStationId - 0.001*EndStationId
         + 20.29*Evening + 0.0003*Income
         + 107.2*PctNoVehicle - 0.088*TripDuration + 0.67*Distance

**Prescriptive Analytics**

Five stations analyzed: Murray Hill, Lincoln Square, Brooklyn, East Village, Lower East Side

Optimization model based on August 1, 2018 usage data and 500 available bikes

Trip demand and station interactions considered

**Recommendations**

To meet demand and maximize 715 daily trips with 500 bikes:

• East Village: 224 bikes

• Lower East Side: 114 bikes

• Murray Hill: 95 bikes

• Lincoln Square: 66 bikes

• Brooklyn: 0 bikes

This allocation strategy ensures high-demand areas are prioritized while unused stations like Brooklyn are deprioritized. Citi Bike can replicate this model for future dates and more stations.
