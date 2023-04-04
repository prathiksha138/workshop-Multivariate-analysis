# workshop-Multivariate-analysisAIM:
## AIM:
     To perform Bivariate/Multivariate Analysis for the given data set.
## CODE:
/*
~~~
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_excel("/content/FlightInformation.xlsx")
df.head()
df.isnull().sum()
df.info()
df['Route']=df['Route'].fillna(df['Route'].mode()[0])
df['Total_Stops']=df['Total_Stops'].fillna(df['Total_Stops'].mode()[0])
sns.scatterplot(df['Duration'],df['Destination'])
sns.barplot(x=df["Price"],y=df["Source"],data=df)
airline=df.loc[:,["Airline","Price"]]
airline=airline.groupby(by=["Airline"]).sum().sort_values(by="Price")
plt.figure(figsize=(17,7))
sns.barplot(x=airline.index,y="Price",data=airline)
plt.xticks(rotation = 90)
plt.xlabel=("AIRLINE")
plt.ylabel=("PRICE")
plt.show()
sns.boxplot(df['Price'],df['Duration'])
sns.displot(df, x="Source", hue="Airline")
df.corr()
sns.heatmap(df.corr(),annot=True)
~~~
*/

## OUTPUT:

![image](https://user-images.githubusercontent.com/103166779/193091025-4e056669-34f9-4750-8144-c3362394027d.png)

![image](https://user-images.githubusercontent.com/103166779/193091474-b44d5430-acd5-4c32-bb17-7db15b60e3cc.png)

![image](https://user-images.githubusercontent.com/103166779/193091989-ba5afdc5-ad4a-4c29-b0db-f4b7987e4fc3.png)

![image](https://user-images.githubusercontent.com/103166779/193092243-12cefe29-6a0f-4dee-ad2e-dd56ccbf2c30.png)

![image](https://user-images.githubusercontent.com/103166779/193092424-c5861470-b012-489e-8a29-a77d6336039b.png)

![image](https://user-images.githubusercontent.com/103166779/193092588-30822169-3ba4-4546-b5e5-fb78f047f433.png)

![image](https://user-images.githubusercontent.com/103166779/193092827-5f2f93c2-0e54-4fba-b412-2845f8f900a1.png)

![image](https://user-images.githubusercontent.com/103166779/193092980-4a405690-cd56-4cd4-9532-2deee6d4f8d0.png)

![image](https://user-images.githubusercontent.com/103166779/193093127-3b8e89b2-85a2-4bef-a031-a9a0528ff8b5.png)

![image](https://user-images.githubusercontent.com/103166779/193093259-2c6409f4-7314-4e02-bd60-a1ef0dcac102.png)

![image](https://user-images.githubusercontent.com/103166779/193093388-b9defbed-33c3-4f34-803a-883df82f0e2b.png)

![image](https://user-images.githubusercontent.com/103166779/193093493-a6d74108-6d1d-40af-8b5b-cc3ef670633a.png)


## RESULT:
    Thus the Bivariate/Multivariate Analysis for the given data set is executed successfully.
