# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 31/01/2026

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

# Load the cleaned dataset
data = pd.read_csv("/kaggle/input/time-series/daily-minimum-temperatures-in-me.csv", on_bad_lines='skip')

# Fix columns
data.columns = ["Date", "Temp"]
data["Date"] = pd.to_datetime(data["Date"])
data["Temp"] = pd.to_numeric(data["Temp"], errors="coerce")
data = data.dropna()

# Plot time series
plt.figure(figsize=(12,6))
plt.plot(data["Date"], data["Temp"], color='blue')
plt.title("Daily Minimum Temperatures in Melbourne (1981–1990)")
plt.xlabel("Date")
plt.ylabel("Temperature (°C)")
plt.grid(True)
plt.show()


```







# OUTPUT:

<img width="1116" height="473" alt="image" src="https://github.com/user-attachments/assets/9d3b12ef-fc3a-4dc6-bf31-a56ac666a801" />


# RESULT:
Thus we have created the python code for plotting the time series of given data.
