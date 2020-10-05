# 監督式學習(Supervised Learning)
## 前處理(Processing)
資料讀取-格式調整-填補缺值-去離群值-特徵縮放

### 格式調整
資料變數被分成一類類的，如汽車品牌 : Toyota, Honda, Mazda  
轉成model 可用形式三種方法 :  
1. Drop Categorical Variables  丟掉類別變量    
```
drop_X_train = X_train.select_dtypes(exclude=['object'])
drop_X_valid = X_valid.select_dtypes(exclude=['object'])
```  
2. Label Encoding  把不同值對應不同數字  
```
from sklearn.preprocessing import LabelEncoder
label_encoder = LabelEncoder()
for col in object_cols:
    label_X_train[col] = label_encoder.fit_transform(X_train[col])
    label_X_valid[col] = label_encoder.transform(X_valid[col])
```
3. One-Hot Encoding 替各值增加一行，記錄每筆資料有無此變量  
```
from sklearn.preprocessing import OneHotEncoder
OH_encoder = OneHotEncoder(handle_unknown='ignore', sparse=False)
```
ordinal variables : 有序變量  (適合2)  
nominal variables : 沒明確排序的變量 (適合3，但很多不同值時 ex. >4 也不適合)  

##### K-fold Cross-Validation
將資料拆成k份做交叉驗證，  
選1份當驗證集，剩下k-1份當訓練集，算出一個Validation Error，  
反覆做k次後，把k個Validation Error的值做平均，  
用此值來當模型好壞的指標。  

[scikit-learn](https://scikit-learn.org/stable/index.html)
