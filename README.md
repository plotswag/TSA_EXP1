# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date:19/08/2025

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt
file_path = '/content/cardekho.csv'
data = pd.read_csv(file_path)
yearly_sales = data.groupby("year")["name"].count().reset_index()
yearly_sales.rename(columns={"name": "Sales_Volume"}, inplace=True)
plt.figure(figsize=(12,6))
plt.plot(yearly_sales["year"], yearly_sales["Sales_Volume"], color='blue', linewidth=1, marker='o')
plt.title("Car Sales Volume over Years (Cardekho Dataset)")
plt.xlabel("Year")
plt.ylabel("Sales Volume (Number of Cars)")
plt.grid(True)
plt.show()
```
# OUTPUT:
<img width="1472" height="712" alt="image" src="https://github.com/user-attachments/assets/46e265cd-f182-42ce-87de-0b0f39d31c72" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
