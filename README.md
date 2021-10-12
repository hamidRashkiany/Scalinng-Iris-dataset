# Scalinng-Iris-dataset
<p>In iris dataset, normalize the value of each columns in dataset</br>
Answer:</br>
There are three methods to implement normalization in this dataset:</br>
<h3>Method 1: </h3></br>
Implement normalization such as MinMaxScalar in each column one by one. You can find the codes, in code file</br>

<h3>Method 2: </h3></br>
Implement normalization such as MinMaxScalar in each column one by one. Same as method one, but it will be one exhausted method if the number of features will be so many. Thus make a list of feature names and implement normalization by for loop. Find the source code in code file in method 2 section.</br> 
<h3>Method 3:</h3></br>
As all columns in dataset are numeric data, thus we can implement scaler to whole dataset to whole columns in one-line code. Note that if there are some categorical data, this approach will not work. The source codes are available in code file in section method 3.
</p>
