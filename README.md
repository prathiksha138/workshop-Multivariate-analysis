# workshop-Multivariate-analysisAIM:
### Aim: 
To Perform Bivariate/Multivariate Analysis
### Algorithm:

1. Read the given data 
2.Get information from the data 
3.Perform the Bivariate/Multivariate Analysis
4. Save the clean data to File

### program:
```
NAME:Prathiksha
REG.NO:212220220028
```
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
df = pd.read_csv("FlightInformation.csv")
df
df.head()
df.info()
df.isnull().sum()
df['Route'] = df['Route'].fillna(df['Route'].mode()[0])
df['Total_Stops'] = df['Total_Stops'].fillna(df['Total_Stops'].mode()[0])
df.isnull().sum()
df.shape
plt.figure(figsize=(8,5))
plt.xticks(rotation = 80)
sns.barplot(df["Airline"],df["Price"],hue=df["Total_Stops"])
states=df.loc[:,["Source","Price"]]
states=states.groupby(by=["Source"]).sum().sort_values(by="Price")
plt.figure(figsize=(8,7))
sns.barplot(x=states.index,y="Price",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("SOURCE")
plt.ylabel=("PRICE")
plt.show()
plt.figure(figsize=(5,7))
sns.scatterplot(df['Source'], df['Price'], hue=df['Destination'])
plt.xticks(rotation = 90)
df_count = df.groupby(by=["Source"]).count()
labels=[]
for i in df_count.index:
    labels.append(i)
plt.figure(figsize=(8,8))
colors = sns.color_palette("Set2")
plt.pie(df_count["Price"], colors = colors, labels=labels, autopct = "%0.0f%%",shadow = True) 
plt.title("Source")
plt.show()
df['Airline'].value_counts()
df['Duration'].value_counts()
df_segment = df.groupby(by=["Total_Stops"]).count()
labels = []
for i in df_segment.index:
    labels.append(i)
plt.figure(figsize=(6,6))
colors = sns.color_palette('pastel')
pie = plt.pie(df_segment["Price"], colors = colors, autopct = "%0.0f%%",shadow = True)
plt.title("Total Stops")
plt.legend(pie[0], labels, loc="upper right")
plt.show()
df_region = df.groupby(by=["Destination"]).count()
labels = []
for i in df_region.index:
    labels.append(i)
    
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
pie = plt.pie(df_region["Price"], colors = colors, autopct = "%0.0f%%",shadow = True)
plt.title("Destination")
plt.legend(pie[0], labels, loc="upper right")
plt.show()
```
### output:
![output](./ds1.png)

![output](./ds2.png)

![output](./ds3.png)

![output](./ds4.png)

![output](./ds5.png)

![output](./ds6.png)

![output](./ds7.png)

![output](./ds8.png)

![output](./ds9.png)

![output](./ds10.png)

![output](./ds11.png)

![output](./ds12.png)

![output](./ds13.png)

![output](./ds14.png)

![output](./ds15.png)

## Result : 
Thus we applied Bivariate/Multivariate Analysis Successfully
