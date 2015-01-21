Tom Lous  
19 Jan 2015  

# Quiz 3
## Question 1

In a population of interest, a sample of 9 men yielded a sample average brain volume of 1,100cc and a standard deviation of 30cc. What is a 95% Student's T confidence interval for the mean brain volume in this new population?

### Answer

Assuming underlying data is iid gaussian

$\frac{\bar X - μ}{S / \sqrt{n}}$

follows Gosset's $t$ distibution with $n-1$ degrees of freedom

Interval $\bar X \pm t_{n-1} S / \sqrt{n}$, where $t_{n-1}$ is the relevant quantile


```r
n <- 9
μ <- 1100
σ <- 30
quantile = 0.975 # is 95% with 2.5% on both sides of the range
confidenceInterval = μ + c(-1, 1) * qt(quantile, df=n-1) * σ / sqrt(n)
confidenceInterval
```

```
## [1] 1077 1123
```

---
