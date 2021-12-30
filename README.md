# House_Rocket_Machine_Learning

# 1. Business Problems

**House Rocket** is a fictiticious company whose business model is the purchase and sale of real estate.

**Purpose:** find the best business opportunities in the real estate market and maximize the company's revenue using machine learning modeling. 

**Strategy:** buy properties in good condition at low prices and then resell them at higher prices. 

The dataset used in this projetc contains house sales price for King County (USA) in the period between May 2014 and May 2015. It is available on [Kaggle - House Sales in King County](https://www.kaggle.com/harlfoxem/housesalesprediction). 

House Rocket's CEO asked for a machine learning model to make better decisions in their real estate business model. To help to take decisions, he set the following **business problems**:

- 1. What properties should we purchase and at what price?
- 2. After the properties are in the company's possession, what is the best time to sell them and what would the sale prices be?
- 3. Should House Rocket do a renovation to raise the sale price? What would be the suggestions for changes? What is the price increase given for each refurbishment option?

# 2. Business Assumptions (Formulated Hypothesis)

**Assumptions (hypothesis)** were formulated in order to be tested.

1. Properties **located in Seattle** are **5% more expensive**, on median, than those located in other cities;
2. Properties with **basement** are **20% more expensive**, on median, than those without basement;
3. Properties which were **renovated after 2000's** are **45% more expensive**, on median, than those without renovation and **20% more expensive**, on median, than those renovated before 2000's;
4. Properties **constructed after 2000's** are **2% cheaper**, on median;
5. The **property prices** are **related to the day of week, to the month, to the year and to the season**. 

# 3. Solution Strategy

**Step 01 - Exploratory data analysis:** the main goal is better understand the dataset by applying statistics metrics as well as identifying missing values and outliers.

**Step 02 - Feature selection:** identifying the most important attributes related to the price.

**Step 03 - Assumptions test (Hypothesis test):** testing the formulated hypothesis.

**Step 04 - Feature Engineering:** Developing new variables based on the original features in order to better describe the phenomenon to be modeled. 

**Step 05 - Machine Learning Model:** Training and selecting the Machine Learning model to determine the best parameter values. 

**Step 06 - Insights:** the highlight of the main insights.

**Step 07 - Conversion of insights:** converting insights into business results.

# 4. Top 4 Data Insights

**Hypothesis 2:** Properties with basement are 20% more expensive, on median, than those without basement.

**True.** Properties with basement are, approximately, 25% more expensive than those without basement. Thus, we may construct a basement and enhance the price sale in 25%. 

**Hypothesis 3:** Properties which were renovated after 2000's are 45% more expensive, on median, than those without renovation and 20% more expensive, on median, than those renovated before 2000's.

**True.** Properties which were **NOT** renovated are 95.77% of the dataset and those which were renovated after 2000's are more expensive. However, properties renovated in 2010's are 19% and 15%, on median, cheaper than those renovated in 2000's and 90's, respectively. Furthermore, properties renovated in 2010 are 51.12% and 52.1% more expensive, on median, than those renovated in 60's and 50's, respectively. Therefore, **(1)** there are lots of available properties to be purchased and renovated; **(2)** we may incrase the price of the properties renovated in 2010's in order to match the value of those renovated in 90's and in 2000's; **(3)** we may renovate properties which were renovated in 60's and in 50's - since it is been a long time - and hence to increase more than 50% of their prices.

**Hypothesis 4:** Properties constructed after 2000's are 2% cheaper, on median.

**False.** Properties constructed after 2000's are more expensive. The 2000's is the decade with the highest construction percentage (16.28%). Properties constructed in 2010's are 42.09% more expensive, on median, than those constructed in 60's. This give us the possibility to purchase cheaper 60's properties, renovated them, and resell them with prices from 42 to 52% higher. 

**Hypothesis 5:** The property prices are related to the day of week, to the month, to the year and to the season.

**True.** (5.1) Day of week: Saturday and sunday are the days which properties are least purchased. Each one has 1.33% and 1.06% of total sales, respectively. Even so, they have have the highest median prices which are 475000.0 and 471250.0 dollars, respectively. Thus, we can make a sale on these days in order to sell more properties. Furthermore, as tuesday is the highest percentage sale day (21.81%), we may choose specific properties to sell on this day to increase profit. 

**True.** (5.2) Month: The month with the smallest number of properties sold is January (4.5%) and the highest is May (11.2%). The lowest median price is for February: 426045.0 dollars. The highest median price is for April: 477000.0 dollars. So we may purchase properties in February (due to the lowest prices) and resell them in April (highest prices) to increase profit.

**True.** (5.4) Season: The lowest median price is for winter: 435000.0 dollars. Winter is the season which properties were least sold (16.94%). The highest median price is for spring: 470000.0 dollars. Spring is also the season which properties were most sold (31.86%). This suggests to purchase properties in winter and resell them in spring. 

# 5. Business Results

The following business results were achieved.

| Total Purchase cost (USD) | Total renovation cost (USD) | Total cost (USD) | Total sales price (USD) | Profit (USD) | Profit Percentage (%) |
|:-------------------------:|:---------------------------:|:----------------:|:-----------------------:|:------------:|:---------------------:|
|         1502750.00        |          189000.00          |     1691750.00   |        2967040.00       |  1275290.00  |          75.38        |      

# 6. Conclusions 

It was reached a profit of $ 1,275,290.00 (75.38%) by using Multiple Linear Regression as the Machine Learning model and by choosing the following characteristics:

- 5-bedrooms properties. 
- Properties with less than 3 bathrooms.
- 9000.00 dollars as the cost to add each bathroom. 
- Condition feature equals to or higher than 3.
- Properties with living area larger than 1900 ft².
- A limit price of 260000.00 dollars to purchase the properties.
- April as the month to resell the properties.
- A minimum profit margin of 10%. 
- No basement. 

# 7. Next Steps

Use **artificial neural networks (RNAs)** to make sales decisions.
