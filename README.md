# Evaluation & Analysis of Sales for Peacock Solar

___

#### In the following project the objective is to analyze and evaluate the  Sales Data which was provided to us. So that, we could produce strategies and ideas to increase the sale for the number of Solar Panels for Peacock Solar.

## The major steps to analyse and predict solutions from the data:-

1. IMPORTING LIBRARIES AND DATA
2. MANIPULATING THE DATA
3. DATA VISUALIZATION
5. CONCLUSION

## 1. IMPORTING LIBRARIES AND UNDERSTANDING THE DATA

We will import the pandas library, matplolib library and numpy library as follows:-

```python
import pandas as pd

import matplotlib.pyplot as plt

import numpy as np
```



Now we will import the data file:-

```python
data=pd.read_excel("C:/Users/Sukriti Macker/Peacock Solar Data Analytics Intern/Sales.xlsx")
```


 After examination of the data it was found that there are few major features that would contribute to the analysis of sales data. These features are:-

1. **The city in which lead is present**

2. **The average monthly bill of the lead**

3. **The occupation of the lead**

4. **The number of heavy appliances used by the lead**

5. **Whether the lead has a power backup**

Hence these features were deeply assessed and cleaned by me.

As I observed there are lot of other irrelevant features which would not contribute towards enhancing the prediction results.

Hence to get rid of them we use the following code:-

```python
data.drop(labels=[0,1],axis=0,inplace=True)
```



> Using the .drop() function would help us drop columns which we find unwanted.

> axis=1 will ensure that the column is dropped.

## 2. MANIPULATING THE DATA

The data will be edited to maintain uniformity and consistency. Also, we will fill up the NaN or None value using mean, median or mode.

Missing values or NaN values are present in the dataset when the customer or a layman is used to fill the form for collection of data. This leads to inconsistency in the data which is collected at last.

* Mean is used when the data is numeric, symmetrical and uniform and does not have any outliers.

* Median is used when data is numeric, left skewed or right skewed and consists of outliers.

* Mode is used when working with categorical data. 

We use the following python command to fill NaN or None values, which are also called as missing values:-

```python
data["Lead Interested ...?"].fillna(data["Lead Interested ...?"].mode()[0],inplace=True)
```

Note that the above code to fill NaN values in the column "Lead Interested ...?" uses mode, as the data present in the column is categorical.

```python
data["No. of Heavy Appliances in the House"].fillna(data["No. of Heavy Appliances in the House"].median(),inplace=True)
```

Note that the above code to fill NaN values in the column"No. of Heavy Appliances in the House" uses median, as the data present in the column is numeric, has certain outliers, is slightly left skewed.

> The skewness and outliers can be detected by the use of a histogram.

The following code can be used to plot a histogram of the column "No. of Heavy Appliances in the House"

```python
l=list(data['No. of Heavy Appliances in the House'])
plt.hist(l)
plt.show()
```

## 3. DATA VISUALIZATION

We must visualize the data by plotting graphs as to see the relationship between the top features that effect the target value or the output, which in our case is to analyze the sales of solar panels.

Observing the data would lead us to create newer insights and would bring out an elaborate view of which section of customers are more drawn towards investing in Solar Panels. 

Through this observation, the company can expand their customers in that specific section.

#### 3.1. City

The following graph has been prepared by me through which I analysed that in which city there were maximum and minimum number of leads:-


ANALYSING THE LEADS WHICH PURCHASED THE SOLAR PANELS [Orange Bins]

___

> From the graph it can be clearly observed that the **MAXIMUM NUMBER OF LEADS** WHO ARE **INTERESTED** IN INVESTING IN SOLAR PANELS IS GENERATED **FROM INDORE**

ANALYSING THE LEADS WHICH DID NOT PURCHASED THE SOLAR PANELS [Green Bins]

___

>  Here we can derive another conclusion that, the **MAXIMUM NUMBER OF LEADS** WHO ARE **NOT INTERESTED** IN **JAIPUR**



**Reason for Denial of Solar Panel in Jaipur**


 As we can clearly observe that:-

1. **46.2%** of the leads who are not interested in installing solar panels have **not given a specific reason for denial.**

2. **23.1%** of the leads who are not interested in installing solar panels find the **cost of the solar panels to be extremely high.**

3. The rest of the leads have miscellaneous reasons for denial for example: lead looking for government subsidy, the lead approached another company for solar panels, etc.

4. There should be efforts from the sales department to work on the above mentioned factors and improve the sales.

   

#### 3.2. Average Monthly Bill

The amount of money that the lead spends on electricity bill, plays a key role for the lead to invest in Solar Panels. It helps us understand whether the lead will purchase the solar panel or not. 

This is because, if the customer's electricity bill is huge, he/she may want to invest in solar panel, as in the long run it would reduce the electricity bill and that amount of money can eventually be saved.

I categorized the average monthly bill into three parts:-

1. Average monthly bill between 0-10,000 Rupees  
2. Average monthly bill between 10,000-20,000 Rupees 
3. Average monthly bill above 20,000 Rupees 


ANALYSING THE LEADS WHICH PURCHASED THE SOLAR PANELS [Blue Bins]

___

> The leads having the average monthly bill between **0-10,000 Rupees yield as the MAXIMUM INTERESTED.**



#### 3.3. Occupation of Customer

The profession of the lead is vital in determining whether the lead will be interested in solar panel installation or not.

The occupation is directly linked to the source of income of the lead. If the lead has a decent source of earning, he/she would be in turn drawn towards investing in solar panels.

The following pie chart would elaborately explain that which profession of the lead derives most interested leads who are keen on purchasing solar panels.


After studying the following pie chart we observe that:-

1. The majority category investing in Solar Panels is of business man, with a share of 88.1%
2. Next major sector investing in Solar Panels is Government Employees, with a share of 6.0%

The Sales in these sectors determine the majority sales of solar panels. 













#### 3.4. Number of Heavy Appliances


ANALYSING THE LEADS WHICH PURCHASED THE SOLAR PANELS [Green Bins]

___

> The maximum number of leads are those who have the number of heavy appliances between 0-5.



ANALYSING THE LEADS WHICH DID NOT PURCHASED THE SOLAR PANELS [Black Bins]

___

> The maximum number of customers who did not purchase who have the number of heavy appliances between 0-5.



#### 3.5. Power Backup


ANALYSING THE LEADS WHICH PURCHASED THE SOLAR PANELS [Red Bin]

___

> The maximum number of leads are those who do not have power backup.



ANALYSING THE LEADS WHICH DID NOT PURCHASED THE SOLAR PANELS [Orange Bin]

___

> The maximum number of leads are those who do not have power backup.



## 4. CONCLUSION

 From the Sales Data Analysis, it is observed that the category contributing to the maximum number of sales is also somewhat responsible for the downfall of sales.

1. The sales department should be aware as to why the customers are interested in our company Peacock Solar for the installation of solar panels, so that we could understand customer behavior and increase the number of customers who are not interested.

By understanding the reasons of the customers buying solar panel we could persuade the ones who are not interested.

2. Also, the sales team should note the reasons as to why the customers are not willing to buy solar panels. This is to improve the sales pitch for the future and make any changes in the company's sales strategies.

As we observe from this pie chart:-


It is observed that out of the majority of the customers who showed interest, which happens to be 94% only 6% installed the Solar Panel.
