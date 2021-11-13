# Pure-EDA-Practice

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/RJBraith/Pure-EDA-Practice/HEAD)
---

### 3. World Bank Data EDA

**Python Version:** 3.9  

**Libraries Used:** Pandas, Numpy, World_bank_data, Plotly, Matplotlib, Seaborn.

World_bank_data is a library that makes api calls to the world bank data bank so you can pull data from various indexes without having to download them.

The end goal of this project was to look at some global data provided by the world bank and produce some interactive choropleth maps using plotly.
I also set out to take the data and extract some useful information from it, producing some graphs

Since I found myself wanting to produce identical graphs for the data, I found this great practice for creating graphs with loops. Not all of them are visibly useful because of the scale of the data, but it was a great exercise regardless.

I am very happy with the produces choropleth maps

---

### 5. Ecommerce Dataset
[Link to kaggle page](https://www.kaggle.com/prachi13/customer-analytics)

**Python Version:** 3.9  

**Libraries Used:** Pandas, Numpy, Matplotlib, Seaborn.

Initially I set out with no specific goal in mind, I soon made it a point to practice using pandas built in graphing tools and putting labels on the graphs in addition to the standard, basic data exploration.

I think the graphs turned out nice, adding the value to the centre makes understanding the graph at a glance much easier.

---

### 7. Marriage Data - Women By Age

**Python Version:** 3.9  

**Libraries Used:** Pandas, Numpy, Matplotlib, Seaborn, Scipy.

Data obtained from table 4 of the [ONS publications](https://www.ons.gov.uk/peoplepopulationandcommunity/birthsdeathsandmarriages/marriagecohabitationandcivilpartnerships/datasets/marriagesinenglandandwales2013).

Driven by curiosity I wanted to view the quantity of marriages taking place. This exploration focuses on the number of same-sex marriages from 1900 to 2018.

My first port of call was cleaning and formatting the excel spreadsheet and fixing a typo (2014 listed as 20145). To reduce visual clutter in the plots and their legends I combined the age groups into 10-year bands as opposed to the 5-year bands in the spreadsheet, The cost in terms of granularity is offset by the gain in legibility in my opinion.

I performed a basic pearsonR correlation test on the time series to see if there was a strong time-marriage correlation, In terms of the whole series, 1900-2018, there is a weak negative correlation (-0.137) paired with an equally weak P-value of 0.138 (greater than the standard 0.05 threshold of significance) suggesting that any correlation between time and the total number of marriages is not to be believed. However, splitting the series into two, either side of 1960 creates two statistically significant correlation coefficients.

Before 1960, the time-marriage correlation coefficient suggests a strong positive relationship (0.717) with an exceedingly small P-value of around 1.77e-10.
After 1960, the time-marriage correlation coefficient suggests a very strong negative relationship (-0.922) with an extremely small P-value of around 9.87e-25.

I created a plot of the distribution of total marriages over the period, the correlation coefficients both before and after 1960 attest to the shape of the distribution however there is an inexplicable dip in marriages in the years surrounding 1960

Following this plot I created a line plot by age group, I used a log scale on the Y-axis to separate the less represented age groups and increase legibility. While this slightly harms how easy it is to interpret the graph at face value, it does translate the core 'increase' or 'decrease' message of the age groups over time.

Finally, I selected two years, 1990 and 2018 and calculated the percentage difference in marriages per age group. I centred the change on 0 so that negative changes are visible at a glance. Looking at this data, in particular, there is a 31% reduction in the marriage of women from 1990 to present, The bar chart helps to demonstrate where the changes occur: 

![image](https://user-images.githubusercontent.com/68555817/133647680-8424960e-5816-4aad-ad50-ba79dd09edf9.png)

There was a 94% decrease in marriages of women under 20, along with a 60% decrease in marriages of women aged 20 to 29, The older age groups all saw increases in marriages with the largest increase being women aged 50 to 59 which increased by 149% in the 30 years suggesting people are foregoing marriage early on in life for some reason or another
