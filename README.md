# workshop-Multivariate-analysis
# AIM:
To perform multivarient analysis on the given data set.

# ALGORITHM:
# STEP 1:
   Clean the data
# STEP 2:
   Remove outliers
# STEP 3:
   Apply the skew function and Kurtosis
# STEP 4:
   Apply Bivariate analysis on numerical and categorical
# STEP 5:
   Apply Multivariate analysis.

# CODE
```
NAME:VAISHNAVI S
REG NO:212222230165
```
## Bivariate Analysis
```
import pandas as pd
import seaborn as sns
df=pd.read_csv("FlightInformation.csv")
df

df.isnull().sum()

df.info()

df['Route']=df['Route'].fillna(df['Route'].mode()[0])
df['Total_Stops']=df['Total_Stops'].fillna(df['Total_Stops'].mode()[0])
df.isnull().sum()

sns.scatterplot(x=df["Price"],y=df["Airline"],data=df)

sns.boxplot(x=df['Price'],y=df['Source'],data=df)

sns.barplot(x=df['Price'],y=df['Destination'],data=df)

sns.displot(df,x="Source",hue="Destination")
```
## Multivariate Analysis 
```
df.corr()

import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
df= pd.read_csv("FlightInformation.csv")
df= np.random.randint(low = 1, high = 100, size = (10,10))
print("The data to be plotted:\n")
print(df)
hm = sns.heatmap(data=df)
plt.show()
```
# OUTPUT

# Bivariate Analysis

# DATA SET
![Screenshot 2023-04-04 113650](https://user-images.githubusercontent.com/118541897/229703423-937ff335-2eef-47a3-b1c1-33911170f0a1.png)


# INFO
![Screenshot 2023-04-04 113701](https://user-images.githubusercontent.com/118541897/229703572-766de0cc-eca0-4482-a51b-6e985ca5e678.png)


# DETECTING NULL AS PD
![Screenshot 2023-04-04 113711](https://user-images.githubusercontent.com/118541897/229703651-6db6f8f6-d2e4-4cf8-b22c-315a41f6267f.png)


# REMOVING NULL DATA
![Screenshot 2023-04-04 113719](https://user-images.githubusercontent.com/118541897/229703683-61853a8e-f5d1-4a96-94d5-b0d708c25458.png)


# NUMERICAL & NUMERICAL:

# SCATTER_PLOT
![Screenshot 2023-04-04 113728](https://user-images.githubusercontent.com/118541897/229703726-d883646b-62ee-4967-9da7-edd83b5a5373.png)


# NUMERICAL & CATEGORIAL:

# BOX PLOT
![Screenshot 2023-04-04 113740](https://user-images.githubusercontent.com/118541897/229703992-908fec05-cd71-4d39-ba24-23c3746b4b66.png)


# BAR PLOT
![Screenshot 2023-04-04 113748](https://user-images.githubusercontent.com/118541897/229704024-63302889-dc97-433a-bd76-423355018c83.png)


# DIST PLOT
![Screenshot 2023-04-04 113755](https://user-images.githubusercontent.com/118541897/229704089-fffdafd8-cee5-45af-af85-a6206c6053fc.png)


# MULTIVARIENT ANALYSIS

# CORRELATION
![Screenshot 2023-04-04 114700](https://user-images.githubusercontent.com/118541897/229704256-dbad8351-1a00-4614-b2e7-53fb4c947022.png)


# HEAT MAP
![Screenshot 2023-04-04 113808](https://user-images.githubusercontent.com/118541897/229704177-528a157e-6c66-4167-86ae-bf821c5b8c2b.png)


# RESULT
Thus the Bivariate and Multivariate analysis is observerd for the given data set.
