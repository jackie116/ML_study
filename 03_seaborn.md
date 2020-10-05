# [seaborn](https://seaborn.pydata.org/)
```
import matplotlib.pyplot as plt
import seaborn as sns
```  
設定圖表長寬   
```
plt.figure(figsize=(14,7))
```  
設定標題  
```
plt.title("Average Arrival Delay for Each Airline, by Month")
```  
設定X軸名稱
```
plt.xlabel("Airline")
```  
***
### Trends
折線圖 (Line charts)  
```
sns.lineplot(data=spotify_data)
```  
### Relationship
長條圖 (Bar charts)  
```
sns.barplot(x=flight_data.index, y=flight_data['NK'])
```  
熱點圖 (Heatmaps)  
```
sns.heatmap(data=flight_data, annot=True)
```  
散布圖 (Scatter plots)  
```
sns.scatterplot(x=insurance_data['bmi'], y=insurance_data['charges'])
```  
散布圖+回歸線(regression line)  
```
sns.regplot(x=insurance_data['bmi'], y=insurance_data['charges'])
```  
顏色散布圖 (Color-coded scatter plots)  
```
sns.scatterplot(x=insurance_data['bmi'], y=insurance_data['charges'], hue=insurance_data['smoker'])
```  
lmplot結合regplot與FacetGrid，能同時比較三種變數  
```
sns.lmplot(x="bmi", y="charges", hue="smoker", data=insurance_data)
```  
分類散布圖 (categorical scatter plot)  
```
sns.swarmplot(x=insurance_data['smoker'], y=insurance_data['charges'])
```  
### Distribution
直方圖 (histograms)  
```
sns.distplot(a=iris_data['Petal Length (cm)'], kde=False)
```  
核心密度圖 (kernel density estimate (KDE))  
```
sns.kdeplot(data=iris_data['Petal Length (cm)'], shade=True)
```   
二維密度圖 (two-dimensional (2D) KDE plot)  
```
sns.jointplot(x=iris_data['Petal Length (cm)'], y=iris_data['Sepal Width (cm)'], kind="kde")
```  

***  
#### 設定style
themes  
(1)"darkgrid" (2)"whitegrid" (3)"dark" (4)"white" (5)"ticks"  
```
sns.set_style("dark")
```  
