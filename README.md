# Ex-08-Data-Visualization-
### Reg No - 212221040077 
### Date - 
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Clean the Data Set using Data Cleaning Process

## STEP 3
Apply Feature generation and selection techniques to all the features of the data set

## STEP 4
Apply data visualization techniques to identify the patterns of the data.

# CODE
```python
import pandas as pd
df=pd.read_csv("Superstore.csv",encoding='unicode_escape')
df.head()
```
## DATA VISUALIZATION USING SEABORN :
```
import seaborn as sns
from matplotlib import pyplot as plt
```
### LINE PLOT
```python
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
```
![280221142-ebf5d018-c31c-4610-b26e-6395daeb5448](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/91295ef2-7567-4879-9f1f-3acff4c01169)

![280221177-f50bd4c8-8840-4d61-afa9-f090d98716d2](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/cbbe6935-064a-42e9-8fc8-a3e3051db378)

![280221197-dddc0ce1-5d37-463d-af9d-d9a39cf33def](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/3a194f7e-e863-42af-8172-c2e420db0d74)


### SCATTERPLOT
```python
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
```
![280221332-23b30b9e-cb60-4dd5-a7a7-be941b7e291d](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/fa17bd93-9118-4e1e-a1fd-06b2aee6e602)
![280221367-e422342a-4fff-487e-9780-aa92e2db6b19](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/a9a074be-975a-4337-80ec-9a1f09ddaaa5)
![280221405-8f9e780a-bcdd-47e0-a21e-25e8dca37cab](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/ff179a67-35ff-4ec3-a2b6-ff40fd33f1dd)

### BOXPLOT
```python
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
```
![280221591-68af3f52-c256-452b-b987-afc6767d09ac](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/e8c2fb01-9480-4c1b-bb29-5d8f561d5a45)
![280221620-27f1e245-2725-436d-a68b-df3b3c5c1660](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/959597e8-e10c-4141-98ad-a86f8211d9f3)

### VIOLIN PLOT
```python
sns.violinplot(x="Profit",data=df)
```
![280221737-19b590d7-641d-47ed-af0f-40e52df39587](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/1cb9bdb2-acf1-47e8-aa4a-8d7c15359675)

### BARPLOT
```python
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
```
![280221836-16ece634-b224-42df-82be-c4a731f908af](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/32a54dbb-c69a-4648-93d8-94c35e7d69e7)
![280221914-32fcf2ae-85be-4bfa-bacb-0839304efe5b](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/920c2dab-16ad-4744-8efc-c940b0f88c3c)

### HISTOGRAM
```python
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
``` 
![280222156-6e5a4fab-1cfd-4415-9a76-6e398571742b](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/602511cf-9ac3-4413-bbfd-198232900fef)

### KDE PLOT
```python
sns.kdeplot(x="Profit", data = df,hue='Category')
```
![280222235-2129a043-381c-4b04-a0da-5b6745ba0adf](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/22103f54-d148-4a89-ba62-068a9d9d4fc3)

## DATA VISUALIZATION USING MATPLOTLIB :
### LINE PLOT
```python
plt.plot(df['Category'], df['Sales'])
plt.show()
```
![280224173-5f621aad-c520-4e01-96cf-1701acefa1e7](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/15663533-8d6c-4fc1-b9df-94d0fa2fe846)

### HEATMAP
```python
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```
![280224277-d133809e-1704-4f91-8332-0041d7ca3e33](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/aaa31e48-495c-45e7-852d-ea2289110546)


### HISTOGRAM
```python
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
```
![280224500-5d549a00-18a3-4126-af87-1652098f826d](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/d665fa55-4a7c-4d2a-bcdd-17ed03f97bcf)

### BARGRAPH 
```python
plt.bar(df.index,df['Category'])
plt.show()
```
![280224538-bee209ed-e0f9-4968-94c7-babc9140edfb](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/04580e06-0224-4db0-addd-adfaae323a6a)

### SCATTERPLOT
```python
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
```
![280224583-82653e8a-3f2a-4a58-ae41-0631925cd402](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/a6d33218-0ec7-41bf-9a07-296062f8285a)

### BOXPLOT
```python
plt.boxplot(x="Sales",data=df)
plt.show()
```
![280224625-9515bcd2-15ba-453a-a02e-e3e6e3ea875c](https://github.com/Anbuselvan04/ODD2023-Datascience-Ex-08/assets/119410896/d7a39ddf-f238-492b-ba93-7e64032627b1)

# RESULT:
Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.
