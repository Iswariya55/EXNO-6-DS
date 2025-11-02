# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 ```
 import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("titanic_dataset.csv")
 df.head()
```
<img width="1581" height="453" alt="image" src="https://github.com/user-attachments/assets/f320c008-4d3c-4a7b-be91-091acca1c2e7" />

 1.Line Plot
 ```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```
<img width="756" height="586" alt="image" src="https://github.com/user-attachments/assets/04531214-72f4-48d5-9eb2-2e7682ddfe3e" />

 2.Multi Line Plot
 ```
 x=[1,2,3,4,5]
 y1=[3,5,2,6,1]
 y2=[1,6,4,3,8]
 y3=[5,2,7,1,4]
 sns.lineplot(x=x,y=y1)
 sns.lineplot(x=x,y=y2)
 sns.lineplot(x=x,y=y3)
 plt.title('Multi Line Plot')
```
<img width="880" height="586" alt="image" src="https://github.com/user-attachments/assets/3131d89e-fc29-4a86-b814-578c106e6cae" />

 TO VISUALIZE RELATIONSHIPS
  1.Bar Chart
  ```

 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```
<img width="1021" height="652" alt="image" src="https://github.com/user-attachments/assets/320d1b42-9af6-4ee0-b679-86605c55034c" />

 2.Scatter Plot
 ```
 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```
<img width="806" height="594" alt="image" src="https://github.com/user-attachments/assets/4735219e-c853-4a27-8e72-2ecfb5be1e98" />

 3.Bubble Chart
 ```

 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```
<img width="834" height="579" alt="image" src="https://github.com/user-attachments/assets/37a70d10-3dbd-48ef-93a8-63d102e6ed36" />

 TO CAPTURE DISTRIBUTIONS
  1.Histogram
  ```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="834" height="557" alt="image" src="https://github.com/user-attachments/assets/b0378de8-704f-4651-a182-b8bd073e80e1" />
 2.Box Plot
 ```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```
<img width="804" height="660" alt="image" src="https://github.com/user-attachments/assets/27a31c0c-4418-4b6b-93e0-edd3c51454cd" />
 3.Violin Plot
 ```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```
<img width="830" height="597" alt="image" src="https://github.com/user-attachments/assets/e10d130e-6b05-4d73-a6ca-10f6991afa64" />

 4.Density Plot
 ```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```
<img width="806" height="611" alt="image" src="https://github.com/user-attachments/assets/81d81d20-376e-4ac0-b17c-3678d082d541" />
 5.Heatmap
 ```
 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```
<img width="816" height="706" alt="image" src="https://github.com/user-attachments/assets/9f9cd37f-fc78-4a87-80c7-0c75f911a172" />



# Result:
 
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
