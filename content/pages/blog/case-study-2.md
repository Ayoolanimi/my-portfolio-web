---
title: GBP vs USD ML Project
slug: case-study-2
date: '2024-10-16'
excerpt: ''
featuredImage:
  url: /images/GBPUSD Scatter Plot.png
  altText: Machine Learning
  styles:
    self:
      borderRadius: x-large
  type: ImageBlock
bottomSections:
  - title: Divider
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-7
          - pl-7
          - pb-7
          - pr-7
    type: DividerSection
  - items:
      - title: Created by Olalekan Oseni
        tagline: ''
        subtitle: >-
          A dynamic junior data scientist and analyst with over 3 years of
          experience working with tools such as Python, SQL, MS Excel, Power BI,
          and Tableau, along with libraries like Pandas, NumPy, Scikit-Learn,
          Matplotlib, and Seaborn. This blog provides an overview of a project I
          worked on, including the code and key details.
        image:
          url: /images/Screenshot 2025-02-05 193005-Photoroom.png
          altText: Company logo
          styles:
            self:
              margin:
                - ml-3
          type: ImageBlock
        colors: bg-light-fg-dark
        styles:
          self:
            padding:
              - pt-6
              - pl-6
              - pb-6
              - pr-6
            textAlign: left
            borderColor: border-neutralAlt
            borderStyle: none
            borderWidth: 0
            borderRadius: none
            flexDirection: row
        type: FeaturedItem
    variant: small-list
    colors: bg-light-fg-dark
    styles:
      self:
        margin:
          - mb-20
        padding:
          - pt-0
          - pl-0
          - pb-0
          - pr-0
        justifyContent: center
      subtitle:
        textAlign: center
    type: FeaturedItemsSection
isFeatured: true
colors: bg-light-fg-dark
styles:
  self:
    padding:
      - pt-5
      - pl-5
      - pb-5
      - pr-5
    textAlign: center
    borderColor: border-light
    borderStyle: none
    borderWidth: 0
    borderRadius: none
    flexDirection: col
type: PostLayout
author: content/data/gbp-vs-usd-ml-project.json
---
**SUMMARY**

This project predicts and finds the correlation between stocks in GBP and USD currencies. I had
sourced my data from Kaggle, performed all necessary data cleaning and manipulation, such as
removing outliers. Then, I developed a Linear Model with which I classified the four (4) selected
columns to two (2) variables before proceeding to create my train and test sets using Linear
Regression. Then, I found my prediction value, calculated my intercept, slope and r-squared values
and then proceeded to finding the correlation using both Pearson correlation and Spearman’s
Rank.

**LINES OF CODE**

```
import pandas as pd
import numpy as np
from matplotlib import pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import StandardScaler
from scipy import stats

df = pd.read_csv('GBPUSD=X.csv')

# Checking for outliers with the threshold value without graph
z = np.abs(stats.zscore(df['Open']))
threshold = 3
outliers = df[z > threshold]
print(outliers.count()) # This line of code returns "empty", showing there are no outliers

# Plotting a scatter plot graph to check for outliersz = np.abs(stats.zscore(df['Open']))
threshold = 3
outliers = df[z > threshold]
df.loc[z > threshold, 'Open'] = df['Open'].median()

z1 = np.abs(stats.zscore(df['High']))
out = df[z1 > threshold]
df.loc[z1 > threshold, 'High'] = df['High'].median()
plt.title("Open vs High")
plt.style.use('bmh')
plt.xlabel("High")
plt.ylabel("Open")

x = df['High']
y = df['Open']

plt.scatter(x,y, color='g', marker='o')
plt.grid(True)
plt.legend()
plt.show() # There are no outliers as all the values fall below 1.40

# Developing a Linear Model for values of trade open, trade close, stock high and low
InVar = df[['Close','High','Low']]
DeVar = df['Open']

x = np.array(InVar)
y = np.array(DeVar)

x_train, x_test, y_train, y_test = train_test_split(x,y, test_size=0.2, random_state=0)

LinReg = LinearRegression()
LinReg.fit(x_train,y_train)

y_pred = LinReg.predict(x_test)

print("The predicted value is: \n",y_pred)
print("The coefficients are: ",LinReg.coef_)
print('intercepts is:', LinReg.intercept_)

# Storing my output in a dataframe named "data"
df1 = {
    'actual':y_test,
    'predicted':y_pred,
    'difference':y_test - y_pred
}
data = pd.DataFrame(df1)
print(data)

# Finding the intercept, slope and rsquared from the model
scaler = StandardScaler()
x = scaler.fit_transform(df[['Open']])
y = scaler.fit_transform(df[['Close']])

sz = len(x)
noVar = 0
coVar = 0
LossSm = 0
msqd = 0

for i in range(sz):
    noVar += (x[i] - np.mean(x))*(y[i] - np.mean(y))
    coVar += (x[i] - np.mean(x))**2

slope = noVar/coVar
intercept = np.mean(y) - slope*(np.mean(x))

print('Slope is: ',slope)
print('Intercept is: ',intercept)

ypred = slope*x + intercept
print('The predicted values are: \n',ypred)

# Determining the rsquared value
for i in range(sz):
    LossSm += (ypred[i] - y[i])**2
    msqd += (y[i] - np.mean(y))**2

rSqd = 1 - (LossSm/msqd)
print('The value for rSquared is: ',rSqd)

# Finding the correlation between each variable using Pearson correlation (default) and Spearman correlation
pcorr = df[df.columns[1:6]].corr()
scorr = df[df.columns[1:6]].corr(method = 'spearman')
print('Pearson correlation is: \n', pcorr)
print('Spearman correlation is: \n', scorr)
```

