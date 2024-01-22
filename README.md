
![Screenshot 2024-01-21 143228](https://github.com/Kailastupe999/Car-Sales-Dashboard/assets/157279720/58fcfab6-37e5-470b-82e1-e0ccb0f7b609)

# Car Sales Dashboard

## Overview

This Power BI project focuses on visualizing and analyzing car sales data obtained from Kaggle. 
The dashboard provides insights into various aspects of the car sales, including key performance indicators (KPIs), trends over time, and geographic distribution.

## Problem statement
- Which cars are the most preferred among customers?
- How is the distribution of car sales across months, and is there any discernible pattern?

## Project Stages
### 1. Data Source and Transformation
#### Data Source: 
The dataset used for this project was sourced from Kaggle.
#### Transformation: 
The data underwent transformations using Power Query Editor in Power BI Desktop to clean and structure it for analysis.

### 2. Power BI Data Loading
The transformed data was loaded into Power BI Desktop for further analysis and visualization.

### 3. Date Table and Measures
A Date Table was created to facilitate time intelligence functions within Power BI.
Various measures, including time intelligence functions and aggregate functions, were implemented to derive meaningful insights from the data.
  >####  Some DAX used in measures
  * `YOY Avg growth = DIVIDE(([YTD Average Price]-[PY-YTD avg price]),[PY-YTD avg price])`
  * `YOY cummu colour = if([YOY Cumulative]>0,"GREEN","RED")`
  * `PY-YTD avg price = TOTALYTD([avg price],SAMEPERIODLASTYEAR(Calender[Date]))`

  * `YOY Avg growth = DIVIDE(([YTD Average Price]-[PY-YTD avg price]),[PY-YTD avg price])`
  * `MTD Cars sold = "MTD Cars Sold:"&
  * 
 FORMAT(TOTALMTD(COUNT(car_data[Car_id]),car_data[Date])/1000,"0.00K")`


### 4. KPIs and Measures
Key Performance Indicators (KPIs) were defined to assess the performance of car sales.
Additional measures were created to support KPI calculations and enhance the analytical capabilities of the dashboard.

### 5. Visualizations
The project includes a variety of visualizations, such as charts and maps, to represent the car sales data effectively.
Visualizations provide a comprehensive view of sales trends, geographic distribution, and other relevant insights.

## Insights

* I noticed that the number of cars sold in the first eight months is pretty much the same as the number of cars sold in the last four months. It seems like the sales were consistent throughout the year.
>![Screenshot 2024-01-22 122252](https://github.com/Kailastupe999/Car-Sales-Dashboard/assets/157279720/95750eed-3eb3-43bc-b7e9-9573ec897e78)

* I noticed a preference among customers for white cars during the analysis, as they appear to be the more favored choice in terms of sales.
>![Screenshot 2024-01-22 122341](https://github.com/Kailastupe999/Car-Sales-Dashboard/assets/157279720/e4a8bb27-144f-4667-bb9a-6e516fd17b38)

* The sales have experienced a substantial growth of 23.5% when comparing the Year-to-Date (YTD) performance of the current year to that of the previous year.
>![Screenshot 2024-01-22 122414](https://github.com/Kailastupe999/Car-Sales-Dashboard/assets/157279720/c8c7e3f5-6c63-4913-8b9b-c018b18fa7e1)
* The average Year-to-Date (YTD) price has shown a 
decrease of 0.79%, indicating a slight drop in pricing compared to the previous period.
>![Screenshot 2024-01-22 122442](https://github.com/Kailastupe999/Car-Sales-Dashboard/assets/157279720/70b0ba68-a145-45bc-9b55-67986949f79c)

* Chevrolet stands out as the top-selling car among the available options






