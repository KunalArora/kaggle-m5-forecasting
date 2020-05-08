# kaggle-m5-forecasting

To check the Kaggle competition, please go to following link
https://www.kaggle.com/c/m5-forecasting-accuracy

### Some general information regarding the competition:
The [Makridakis competitions](https://en.wikipedia.org/wiki/Makridakis_Competitions) (or M-competitions), organised by forecasting expert Spyros Makridakis, aim to provide a better understanding and advancement of forecasting methodology by comparing the performance of different methods in solving a well-defined, real-world problem. The first M-competition was held in 1982. The [forth competition (M4)](https://www.sciencedirect.com/science/article/pii/S0169207019301128) ran in 2018 and featured “100,000 time series and 61 forecasting methods” (source in link). According to forecasting researcher and practitioner Rob Hyndman the M-competitions “have had an enormous influence on the field of forecasting. They focused attention on what models produced good forecasts, rather than on the mathematical properties of those models”. This empirical approach is very similar to Kaggle’s trade-mark way of having the best machine learning algorithms engage in intense competition on diverse datasets. M5 is the first M-competition to be held on Kaggle.

### Goal
Teams have been challenged to **predict sales data** provided by the retail giant Walmart **28 days** into the future. This competition will run in 2 tracks: In addition to forecasting the values themselves in the Forecasting competition, we are simultaneously tasked to estimate the uncertainty of our predictions in the Uncertainty Distribution competition. Both competitions will have the same 28 day forecast horizon.

### Dataset
The dataset of the competition can be downloaded directly by following the competition link or it is available as **m5-forecasting-accuracy.zip file** in this github repo.

The data comprises **3049 individual products from 3 categories and 7 departments, sold in 10 stores in 3 states.** The hierachical aggregation captures the combinations of these factors. For instance, we can create 1 time series for all sales, 3 time series for all sales per state, and so on. The largest category is sales of all individual 3049 products per 10 stores for 30490 time series.

The training data comes in the shape of 3 separate files:

**sales_train.csv:** this is our main training data. It has 1 column for each of the 1941 days from 2011-01-29 and 2016-05-22; not including the validation period of 28 days until 2016-06-19. It also includes the IDs for item, department, category, store, and state. The number of rows is 30490 for all combinations of 30490 items and 10 stores.

**sell_prices.csv:** the store and item IDs together with the sales price of the item as a weekly average.

**calendar.csv:** dates together with related features like day-of-the week, month, year, and an 3 binary flags for whether the stores in each state allowed purchases with SNAP food stamps at this date (1) or not (0).

### Information regarding the python notebooks 
