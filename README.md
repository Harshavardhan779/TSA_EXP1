## Developed By: HARSHAVARDHAN
## Register No: 212222240114
##  Date: 

# Ex.No: 01A  PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data (National stock exchange)


# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3.Use the Date coloumn for tracking the index.
4. Plot the data accordingly which can be altered monthly, or yearly.
5. Display the graph.



# PROGRAM:

 
```python
import pandas as pd
import matplotlib.pyplot as plt

file_path = 'infy_stock.csv'
data = pd.read_csv(file_path)

print(data.head)

data['Date']=pd.to_datetime(data['Date'])

data.set_index('Date',inplace=True)
plt.plot(data.index,data['Trades'],label='temp')
plt.title("Daily Minimum Trades")
plt.xlabel("Date")
plt.xticks(rotation=45)
plt.ylabel("Trades")
plt.grid(True)
plt.legend()
plt.show()

```









# OUTPUT:
![OUTPUT](/1.png)
![OUTPUT](/2.png)
![OUTPUT](/graph.png)





# RESULT:
Thus the python code has created  for plotting the time series of given data successfully.
