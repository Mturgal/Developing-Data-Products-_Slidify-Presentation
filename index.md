---
title       : Predicting Wine Prices
subtitle    : Data Analysis as the New Wine Expert !
author      : Metin Turgal
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Statistics vs. Wine Expert 

1. Orley Ashenfelter, a Princeton economics professor, shows that a statistical analysis can outperform wine experts on predicting quality wine.
2. He has used linear regression with the following features to predict the price 
 + Age (older wines are more expensive)
 + Average Growing Season Temperature
 + Harvest Rain
 + Winter Rain
3. The same method and the data is used for our prediction tool, "Wine Price Prediction" website 

---
## The Model
+ The variables on which the prediction is based on are statistically powerful predictors,as shown below:



```r
summary(lm(Price~AGST+HarvestRain+ WinterRain+Age,data=wine))
```

```
## 
## Call:
## lm(formula = Price ~ AGST + HarvestRain + WinterRain + Age, data = wine)
## 
## Residuals:
##      Min       1Q   Median       3Q      Max 
## -0.45470 -0.24273  0.00752  0.19773  0.53637 
## 
## Coefficients:
##               Estimate Std. Error t value Pr(>|t|)    
## (Intercept) -3.4299802  1.7658975  -1.942 0.066311 .  
## AGST         0.6072093  0.0987022   6.152  5.2e-06 ***
## HarvestRain -0.0039715  0.0008538  -4.652 0.000154 ***
## WinterRain   0.0010755  0.0005073   2.120 0.046694 *  
## Age          0.0239308  0.0080969   2.956 0.007819 ** 
## ---
## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
## 
## Residual standard error: 0.295 on 20 degrees of freedom
## Multiple R-squared:  0.8286,	Adjusted R-squared:  0.7943 
## F-statistic: 24.17 on 4 and 20 DF,  p-value: 2.036e-07
```

---
## Model Variables vs. Wine Price

![plot of chunk unnamed-chunk-3](assets/fig/unnamed-chunk-3-1.png) 

---

## Why Should You Consider It ?

1. It's cheaper than hiring a wine expert.
2. It's convenient : Even from your mobile device you can get a prediction. 
3. It's fast: It doesn't need a time a preliminary research. It is already done ! 
4. Simple and straightforward 
 + It doesn't need any prior knowledge, it can be used easily by anybody.
 

