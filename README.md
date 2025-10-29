# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
# NAME: S.DHAYALAPRABU
# ROLL NO : 212224230065

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
<img width="1554" height="253" alt="image" src="https://github.com/user-attachments/assets/f31d746d-8452-4bc8-9bd5-6856f2d59276" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="662" height="534" alt="image" src="https://github.com/user-attachments/assets/3b2bc080-6d84-4bf1-933a-67d24805f5e6" />

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
<img width="662" height="537" alt="image" src="https://github.com/user-attachments/assets/a54795c3-869e-43ec-bc21-87cbb4ff0e1a" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="712" height="479" alt="image" src="https://github.com/user-attachments/assets/01e77456-90c9-465a-a181-1b7ebfe890af" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="708" height="561" alt="image" src="https://github.com/user-attachments/assets/7952fa93-e430-41b9-bb82-27ff49a7622f" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="712" height="566" alt="image" src="https://github.com/user-attachments/assets/9f726fa2-0db3-464c-b629-d9bc684bc513" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="705" height="531" alt="image" src="https://github.com/user-attachments/assets/2c6a9160-643b-4062-8828-84a5403b409a" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="692" height="559" alt="image" src="https://github.com/user-attachments/assets/728360b8-517f-4e88-a24f-0f2c1c48959a" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="706" height="559" alt="image" src="https://github.com/user-attachments/assets/e05ef0dd-15a6-4e71-8d50-395a32c76c54" />

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="710" height="546" alt="image" src="https://github.com/user-attachments/assets/3f6183e6-385c-4480-935d-a7d4eda82870" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="710" height="597" alt="image" src="https://github.com/user-attachments/assets/9c20e454-ac2f-4dc0-88ad-68688be7eb9a" />


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
