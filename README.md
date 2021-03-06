# Cryptocurrencies

## Overview of the Analysis:

### This project aims to create a report for Accounting Accountabilty, an investment company. This report includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment. Since there is no known output, *unsupervised machine learning* was used to process and cluster data,and, to reduce dimensions and principal components using principal component analysis (PCA) 

## Results:

### After extracting and transforming the data, the following analysis was obtained:

## Cryptocurrencies Data

<p align="center">
  Image 1. Cryptocurrencies DataFrame
</p>

![This is an image](https://github.com/gmgarin/Cryptocurrencies/blob/cdf64ac53c11addbc5b0a6e7d8327529474d714b/images/image1.png)


### The table above shows preprocessed data before reduction using PCA algorithm. The DataFrame was reduced to three pincipal components. Then, an *elbow curve* (Image 3) was created to find the best value for *K* from the DataFrane (Image 2) showing the threee principal components.

<p align="center">
  Image 2. PCS DataFrame
</p>

![This is an image](https://github.com/gmgarin/Cryptocurrencies/blob/cdf64ac53c11addbc5b0a6e7d8327529474d714b/images/image2.png)


<p align="center">
  Image 3. Elbow Curve
</p>

![This is an image](https://github.com/gmgarin/Cryptocurrencies/blob/97fa7aeac85240d43caf2d06d005f9727778cd8f/images/image3a.png)


### As mentioned, the goal of this analysis is to create a classification system for cryptocurrencies. The *K* value = 4 was determined based on the *elbow cruve*. As a result, four prediction clusters were created. 

## Visualization of Results


<p align="center">
  Image 4. 3D - Scatter Plot
</p>

![This is an image](https://github.com/gmgarin/Cryptocurrencies/blob/cdf64ac53c11addbc5b0a6e7d8327529474d714b/images/image4.png)


<p align="center">
  Image 5. First 11 Tradable Cryptocurrencies DataFrame using hvPlot
</p>

![This is an image](https://github.com/gmgarin/Cryptocurrencies/blob/cdf64ac53c11addbc5b0a6e7d8327529474d714b/images/image5.png)

### The data has been standardized and by using PCA, the number of features was reduced. Visualizing the transformed data using 3D scatter plot graph (Image 4) above shows PC 1, PC2, and PC 3 creating three main dimensions of variations that contain most of the information of the original dataset. A generated DataFrame of tradable cryptocurrencies (Image 5) using *hvplot* function determined that there are 532 cryptocurrencies being traded. 

### To futher simplify, another DataFrame (Image 6) was created showing a scaled data from the previous DataFrame. This shows coin names, classification, total supply, and total coins mined. This new data set was also plotted into a simplified scatter plot graph.

<p align="center">
  Image 6. Scaled DataFrame
</p>

![This is an image](https://github.com/gmgarin/Cryptocurrencies/blob/cdf64ac53c11addbc5b0a6e7d8327529474d714b/images/image7.png)


<p align="center">
  Image 7. hvPlot Scatter Plot
</p>

![This is an image](https://github.com/gmgarin/Cryptocurrencies/blob/cdf64ac53c11addbc5b0a6e7d8327529474d714b/images/image6.png)

### Looking at the graph, most cryptocurrencies are classified under classes *0* and *3*. At the same time, many of these tradable tokens have limited public availability and circulation in the market. The total number of coins mined of most cryptocurrencies are under 20%. The graph also shows a general trend that as the total coins mined increases, the number of total coin supply also increases. 

## Summary

### The application of *unsupervised machine learning* in the crypto world is a systematic way to create an intuitive representation. Since public trading of cryptocurrencies has a constantly changing trend, the machine learning algorithm can be utilized to predict trends and/or patterns from the whole dataset to determine which cryptocurrencies are worth the investment. 

#### *Resources:*
##### Dataset from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist)
##### Tools: [Python 3.9](https://www.python.org/downloads/release/python-390/), [scikit-learn 0.24.2](https://scikit-learn.org/stable/whats_new/v0.24.html), [hvPlot 0.8](https://hvplot.holoviz.org/user_guide/Introduction.html), [plotly 5.8.0](https://pypi.org/project/plotly/)
##### Article: [Circulating Supply](https://academy.binance.com/en/glossary/circulating-supply)
