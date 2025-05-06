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
![Screenshot 2025-05-06 191010](https://github.com/user-attachments/assets/cce33967-c5ba-4766-9d7e-bbe1c730fe8a)
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![Screenshot 2025-05-06 191016](https://github.com/user-attachments/assets/603800fc-46b8-44a0-87f7-2564b61c32fd)
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
![Screenshot 2025-05-06 191021](https://github.com/user-attachments/assets/c02f55e9-e13f-47e5-8e22-617c6e7e07eb)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![Screenshot 2025-05-06 191026](https://github.com/user-attachments/assets/9fdcfb6f-7713-4f73-b531-18eb64907484)

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![Screenshot 2025-05-06 191032](https://github.com/user-attachments/assets/bd7e8293-c981-4650-aab5-dffc79586038)

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![Screenshot 2025-05-06 191038](https://github.com/user-attachments/assets/bf851b00-3fee-43b8-b734-b55ed77bdb2d)

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![Screenshot 2025-05-06 191044](https://github.com/user-attachments/assets/dee20af8-af16-46e3-b791-3bb7f696f94a)

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![Screenshot 2025-05-06 191049](https://github.com/user-attachments/assets/7b130273-1f16-467e-b4d5-21eca29f3846)

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![Screenshot 2025-05-06 191054](https://github.com/user-attachments/assets/44ad7219-45cf-4e46-8817-d86172fbc228)

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![Screenshot 2025-05-06 191059](https://github.com/user-attachments/assets/c8aa9bc7-de16-43a0-b350-3a7fa7e8f7df)

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
![Screenshot 2025-05-06 191105](https://github.com/user-attachments/assets/fcbd950d-d267-4fb4-88ec-de807d22b32a)

# Result:
Successfully Performed the Data Visualization using seaborn python library for the given datas.
