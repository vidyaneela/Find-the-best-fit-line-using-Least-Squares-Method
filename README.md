# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: M.Vidya Neela
RegisterNumber:  212221230120
*/
```
```

#import files
import numpy as np
import matplotlib.pyplot as plt

#assign input

X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])


# mean values of input

X_mean=np.mean(X)
print("X_mean =",X_mean)
Y_mean=np.mean(Y)
print("y_mean =",Y_mean)

num=0
denum=0

for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2

# find m
print("find m")
m=num/denum
print("m=",m)

# find b
print("find b")
b=(Y_mean)-(m*X_mean)
print("b =",b)

# find Y_pred
print("find Y_pred")
Y_pred=m*X+b
print("Y_pred =",Y_pred)

#plot graph

plt.scatter(X,Y,color='orange')
plt.plot(X,Y_pred,color='maroon')
print("Graph")
plt.show()

```

## Output:
![192947940-c53b084f-879d-4893-ab43-87e5e1219895](https://user-images.githubusercontent.com/94169318/193605637-909ed129-6510-4ff7-827d-d7b128a3ea79.png)
![192947984-9f7aab55-b666-4d93-b818-fcc186468897](https://user-images.githubusercontent.com/94169318/193605679-f3a3c5e2-24be-441d-8ac1-379ecb3dd079.png)
![192948140-96ac35f6-3c0f-4ce9-9866-1a467788e2f9](https://user-images.githubusercontent.com/94169318/193605703-a8ef68c8-0f18-45d9-b8f6-9d3b781a8f18.png)
![192948255-d4658919-d2db-44ee-a55c-4b0572268da2](https://user-images.githubusercontent.com/94169318/193605737-53bdbcd5-358c-4c21-9e84-5a7aa157e495.png)
![192948353-92eff6f5-bb48-4e90-9b80-9164e3fc476c](https://user-images.githubusercontent.com/94169318/193605787-e3622c1b-9b28-44d5-ab53-6a903fb765f8.png)
![192948420-45f25a8a-513c-4f53-afe7-1f09e9a51797](https://user-images.githubusercontent.com/94169318/193605824-89048523-74fc-4ddf-8ffc-eccde1cd2166.png)
![192948438-fe5a2af6-f3e9-48ab-ab12-9c672cbfca2c](https://user-images.githubusercontent.com/94169318/193605856-2c8f02f9-df84-4f0b-aa17-61418f8e78b3.png)
![192948463-55bc63d6-0fbc-4757-8063-36cc30c57b7b](https://user-images.githubusercontent.com/94169318/193605879-d21d98b9-e261-4b33-a8b6-807b93d0b94e.png)
![192948548-6af9cfb1-0532-4f61-b8c4-fb3ce76ce101](https://user-images.githubusercontent.com/94169318/193605910-36da7aed-4993-4e00-a816-f98643dd5564.png)
![192948493-8562395b-4b3b-4ed8-ae1d-d4dec610a432](https://user-images.githubusercontent.com/94169318/193605943-f87c2613-7f06-458e-8b79-47842dcaaeab.png)
![192948619-5b82d129-d63e-49f2-b1af-08913c76cc52](https://user-images.githubusercontent.com/94169318/193605979-0ff5f125-1ebf-4e7b-844e-ed7f6da756af.png)
![192948623-11c560ba-c7cf-47b4-91a5-1fcdf92fabf8](https://user-images.githubusercontent.com/94169318/193606007-5e471686-c3a1-448e-b1ed-bc3c84638407.png)

##GRAPH:
![192948620-e5449267-d27f-4e6c-b956-fddd6bd751c6](https://user-images.githubusercontent.com/94169318/193606099-2c73f17f-d5ef-4741-8c5f-e4a1ea8bbfef.png)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
