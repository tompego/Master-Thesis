# Master-Thesis
Impact of Renewable Energy on the Shape of German Day-Ahead Energy Market


#Problem Statement:

Each day, energy traders place bids to buy or sell electricity for the following day on EPEX SPOT, the German day-ahead (DA) energy market. The deadline for bids in the energy market is at noon the day before, requiring bidders to estimate for the next day. These bids are for each hour of the day and are used by EPEX SPOT to construct supply and demand curves. The resulting prices derived from these curves are the hourly DA prices, the market price for electricity. 

The hourly DA prices follow specific patterns corresponding to the hour of the day or day of the week, which influence the energy demand in the market. Also impacting price, supply follows specific patterns relating to production, depending on energy source. These relationships are modeled by energy companies to construct Hourly Price Forward Curves, which inform their bids on EPEX SPOT. Therefore, the creation of an accurate shaping model is essential for calibration. Accurate modeling of these prices would allow energy bidders to maximize their revenue (minimize bid to buy, maximize offer to sell).

Research Objective:

This thesis would attempt to model the impact of renewable energy production, particularly wind and solar, on the shape of the hourly (intra-daily) profiles for the energy prices on the German day-ahead market.

Expected Results: 

We would expect that a model utilizing wind and solar production as key inputs would be able to provide a useful estimation of generic intra-daily energy price curves in Germany, given Germany’s high dependence on wind and solar. We expect that research into the development of such a model would provide base shapes to use in conjunction with models of seasonal shapes to calibrate for the purposes of predicting future spot prices of energy.

Methodology/Empirical Approach:

Our study would attempt to model the general shape of hourly prices in the German energy DA market using, as inputs, solar and wind production (normalized), day of the week, hour, and holiday to predict a day to month ratio of price quotes. Our initial variables would be as stated above, but additional data, including macroeconomic data, other renewable energy, and non-renewable energy production, will be evaluated. Additionally, we intend to examine interactions between variables and polynomial transformations in our feature selection process. In order to observe general patterns not impacted by temporal shifts, our model will attempt to predict an hour-to-day ratio of spot price.

To begin our study, we begin by cleaning all of the data, and ensuring no missing or invalid data entries.  We then would move to the training process.  We do this to ensure that our model does not overfit the data and will generalize well enough to accept new data inputs. To accomplish this, we first would use resampling methods. Create an appropriate split for our test data, approximately 10-25% of data for a test set to use later.  Additionally, to validate the training data, we will focus on using k-fold cross-validation.  Cross-validation is the best choice for our particular study, as it ensures we don’t lose any of our limited data to the validation process. Our data is limited to the last 3-5 years due to the restrictive nature of studying renewable energy.  

We intend to evaluate the predictive capability of several models for the purposes of selecting the algorithm which produces the best model of spot price ratios. Of particular interest is the use of artificial neural networks (ANNs), specifically using a feedforward neural networks (FNN), and in addition using a recursive neural network (RNN).  However, gradient boosting and SVM models will be conducted as well. 

Additional research would be conducted to evaluate the impact of the change in ratio of fossil fuel energy production share on EPEX SPOT prices.  Such models would not only focus on renewable energy but instead incorporate the impact of specific fossil fuels’ effect on the shape of the German DA market.  We are specifically interested in the increasing use of natural gas, and the rapidly declining electricity generation from hard coal.  

Data:

Production, consumption, and price data for the German power market
Data will be analyzed using only the past 3-5 years of data, due to the rapidly shifting market of renewable energy. 
Data period estimate:  2018-01-01 - 2022-03-01. 
Data source: German Electricity Market by  https://www.smard.de/en 

