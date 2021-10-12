# Scalinng-Iris-dataset
In iris dataset, normalize the value of each columns in dataset
Answer:
There are two methods to implement normalization in this dataset:
Method 1: 
Implement normalization such as MinMaxScalar in each column one by one.
from sklearn.preprocessing import MinMaxScaler
scaler=MinMaxScaler(feature_range=(0,1))
df[["sepal length (cm)"]]=scaler.fit_transform(df[["sepal length (cm)"]])
df[["sepal width (cm)"]]=scaler.fit_transform(df[["sepal width (cm)"]])
df[["petal length (cm)"]]=scaler.fit_transform(df[["petal length (cm)"]])
df[["petal width (cm)"]]=scaler.fit_transform(df[["petal width (cm)"]])

Method 2:
Implement normalization such as MinMaxScalar in each column one by one. Same as method one, but it will be one exhausted method if the number of features will be so many. Thus make a list of feature names and implement normalization by for loop as below:
from sklearn.preprocessing import StandardScaler
scaler=StandardScaler()
columns_names=["sepal length (cm)","sepal width (cm)","petal length (cm)","petal width (cm)"]
for column in columns_names:
    df[[column]]=scaler.fit_transform(df[[column]])
df.head()

Method 3:
As all columns in dataset are numeric data, thus we can implement scaler to whole dataset to whole columns in one-line code. Note that if there are some categorical data, this approach will not work.
from sklearn.preprocessing import Normalizer
norm=Normalizer()
df=norm.fit_transform(df)
from sklearn.preprocessing import Binarizer
binarizer=Binarizer(threshold=0.0)
df=binarizer.fit_transform(df)
