### Missing Value
1. Drop Columns with Missing Values  
把有缺值的行丟掉，這方法只有在那欄缺很多值時適用  
2. Imputation  
替缺攔補值，例如插入平均值  
3. An Extension To Imputation  
補值外，多增加一行紀錄哪些是有補過的  

### outlier的處理
outlier(離群值,例外值)  

#### outlier出現的原因
* 未知數的隨意填補
* 記錄錯誤  
#### 檢查方式
* 確認欄位意義
* 畫圖或用統計值檢查  
  box plot, scatter plot
#### 處理方式
* 刪除欄位
* 新增欄位紀錄異常
* 填補(中位數(midian),min,max,平均數(mean),眾數(mode),分位數(quantiles)...)
