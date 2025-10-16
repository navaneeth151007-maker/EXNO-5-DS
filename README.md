# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

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
import matplotlib.pyplot as plt
data = pd.read_csv(r"E:\titanic_dataset.csv")
print(data.head())
```
<img width="798" height="493" alt="image" src="https://github.com/user-attachments/assets/cae6602e-ea5b-4e13-98a9-8112d9ab4991" />

```
# Rplt.figure(figsize=(6,4))
data['Pclass'].value_counts().sort_index().plot(kind='bar', color='skyblue')
plt.title('Number of Passengers by Class')
plt.xlabel('Passenger Class')
plt.ylabel('Count')
plt.show()

```
<Figure size 600x400 with 1 Axes><img width="540" height="388" alt="image" src="https://github.com/user-attachments/assets/65219f6b-dec3-480f-96d4-aa1bfb2c573c" />

```
plt.figure(figsize=(6,4))
plt.hist(data['Age'].dropna(), bins=20, color='orange', edgecolor='black')
plt.title('Age Distribution of Passengers')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()
```
<Figure size 600x400 with 1 Axes><img width="540" height="393" alt="image" src="https://github.com/user-attachments/assets/8d5a15ac-64d0-4d73-90c4-04169209ed2b" />

```
plt.figure(figsize=(5,5))
data['Survived'].value_counts().plot(
    kind='pie',
    labels=['Not Survived', 'Survived'],
    autopct='%1.1f%%',
    colors=['lightcoral', 'lightgreen']
)
plt.title('Survival Distribution')
plt.ylabel('')
plt.show()
```
<Figure size 500x500 with 1 Axes><img width="404" height="427" alt="image" src="https://github.com/user-attachments/assets/3ed6cf53-05a7-4383-9587-decd93d35050" />

```
plt.figure(figsize=(6,4))
plt.scatter(data['Age'], data['Fare'], color='purple', alpha=0.5)
plt.title('Age vs Fare')
plt.xlabel('Age')
plt.ylabel('Fare')
plt.show()

```
<Figure size 600x400 with 1 Axes><img width="540" height="393" alt="image" src="https://github.com/user-attachments/assets/7de0288b-e54e-457b-8db7-05250fc72886" />

```
plt.figure(figsize=(6,4))
plt.plot(data['Fare'].head(50), color='green', marker='o')
plt.title('Fare of First 50 Passengers')
plt.xlabel('Passenger Index')
plt.ylabel('Fare')
plt.show()
```
<Figure size 600x400 with 1 Axes><img width="540" height="393" alt="image" src="https://github.com/user-attachments/assets/af5eedee-57ba-4a34-aaa4-25ec9a8f1c4a" />

```
```
Result:
The above program and output Data visualization using MatplotLIB
