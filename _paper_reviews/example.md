---
layout: page
title: Paper Review
description: Paper xxxxxx
date: 2021-10-18
permalink: /paper_reviews/2021-10-18_test_paper_review/
tags:
  - mathematics
  - measure theory
  - probability
  - statistics
  - tutorial
  - measureable function
  - random variable
---

<br />

Introduction
-----

We can define expectation as follows:

$$E(X) := \sum_x xP(X=x)$$  

whereas if $$X$$ is continuous its expectation is given by    

$$E(X) := \int_x x \ f(x) \ dx$$

where $$f(x)$$ is $$X$$'s density function. 



```python
# Python program to check if year is a leap year or not

year = 2000

# To get year (integer input) from the user
# year = int(input("Enter a year: "))

if (year % 4) == 0:
   if (year % 100) == 0:
       if (year % 400) == 0:
           print("{0} is a leap year".format(year))
       else:
           print("{0} is not a leap year".format(year))
   else:
       print("{0} is a leap year".format(year))
else:
   print("{0} is not a leap year".format(year))
```





This is the way to write code