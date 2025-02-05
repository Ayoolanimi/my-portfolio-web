---
title: GBP vs USD ML Project
slug: case-study-2
date: '2024-10-16'
excerpt: >-
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante lorem,
  tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at auctor sapien.
  Etiam at cursus enim. Suspendisse sed augue tortor. Nunc eu magna vitae lorem
  pellentesque fermentum. Sed in facilisis dui.
featuredImage:
  url: /images/img-placeholder.svg
  altText: Case study 2
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
      - title: About Company
        tagline: This is the tagline
        subtitle: >-
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante
          lorem, tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at
          auctor sapien.
        image:
          url: /images/telus-logo.svg
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


```

