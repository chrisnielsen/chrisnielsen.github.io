---
layout: page
title: Math Questions
permalink: /paper_reviews/math-test2/
---
<br />
{% raw %}
<br />
## Open Questions
{: style="text-align: justify"}
---

{: style="text-align: justify"}
This section contains discussion around open questions I have
{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}
<br />
#### Interpretation of min/max operations
{: style="text-align: justify"}
---

{: style="text-align: justify"}
The repo containing the code for this post is located [here]( https://github.com/chrisnielsen/chrisnielsen.github.io)
{: style="text-align: justify"}

{: style="text-align: justify"}
A question I have struggled with that is how to interpret the expression:
{: style="text-align: justify"}

{: style="text-align: justify"}
$$\mathop {\max }\limits_x \mathop {\min }\limits_y f\left( {x,y} \right)$$
{: style="text-align: justify"}

{: style="text-align: justify"}
So far, I think the best way to interpret this expression is the following: consider breaking the expression into two components as follows:
{: style="text-align: justify"}

{: style="text-align: justify"}
$$\mathop {\max }\limits_x \mathop {\min }\limits_y f\left( {x,y} \right) = \mathop {\max }\limits_x g\left( x \right)$$ where $$g\left( x \right) = \mathop {\min }\limits_y f\left( {x,y} \right)$$
{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}
<br />
##### What can we do to fix this
{: style="text-align: justify"}
---

{: style="text-align: justify"}
Therefore, we can interpret this expression as:
{: style="text-align: justify"}
1. Pick an x value that we are evaluating
{: style="text-align: justify"}
2. Evaluate g(x) for that x value (this will return the y value that minimizes f(x,y) for that choice of x)
{: style="text-align: justify"}
3. Repeat step 1 until we find the value of x which maximizes g(x)
{: style="text-align: justify"}

{: style="text-align: justify"}
Another way to interpret the min/max operations is to think about finding the saddle point of a function. Finding the saddle point is equivalent to finding the min/max solution for a set of variables.
{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}
This is a test.
{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}
This is a test.
{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}
<br />
##### Here is a proof that for any function$$f\left( {x,y} \right)$$we have $$\mathop {\max }\limits_y \mathop {\min }\limits_x f\left( {x,y} \right) \le \mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right)$$ 
{: style="text-align: justify"}
---

{: style="text-align: justify"}

{: style="text-align: justify"}
Proof
{: style="text-align: justify"}

{: style="text-align: justify"}
Suppose that $$\left( {{x^*},{y^*}} \right)$$is the optimal solution to $$\mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right)$$, such that $$\mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right) = f\left( {{x^*},{y^*}} \right)$$. This implies that $$\mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right) = \mathop {\max }\limits_y f\left( {{x^*},y} \right)$$since we can view the inner max operation as being evaluated for a specific x value, and since $${x^*}$$is optimal, we can remove the min operation. 
{: style="text-align: justify"}

{: style="text-align: justify"}
Now let use examine the situation where the min and max operations are switched such that $$\mathop {\max }\limits_y \mathop {\min }\limits_x f\left( {x,y} \right)$$. Focusing on the inner min operation: since the inner min operation is the minimum over all x values then $$\mathop {\min }\limits_x f\left( {x,y} \right) \le f\left( {{x^*},y} \right)$$.  Since this inequality must hold for all values of y, the inequality is preserved when we take the max operation of y on both sides of the inequality. Therefore, we have that $$\mathop {\max }\limits_y \mathop {\min }\limits_x f\left( {x,y} \right) \le \mathop {\max }\limits_y f\left( {{x^*},y} \right)$$. Now substituting in the expression from above we have:$$\mathop {\max }\limits_y \mathop {\min }\limits_x f\left( {x,y} \right) \le \mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right)$$, 
{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}
 **An open question remains regarding when the order of min and max can be exchanged.**
{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}
<br />
## Useful General Knowledge
{: style="text-align: justify"}
---

{: style="text-align: justify"}
This section contains general knowledge and tricks about different things that are useful
{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}
<br />
#### Use Cholesky to Sample from Gaussian
{: style="text-align: justify"}
---

{: style="text-align: justify"}
There are a number of python functions that can be used to sample from a multivariate Gaussian. One technique is to sample from a standard Gaussian (i.e. zero mean, identity covariance), and then transform the sample such that it resembles being sampled from a Gaussian with mean m and covariance S. This can be achieved as follows (taken from "Gaussian Processes for Machine Learning slide 9")
{: style="text-align: justify"}

{: style="text-align: justify"}
<figure><center><img src="/assets/img/math-test2/image1.png" alt="Figure 1. Cholesky Algorithm" width="500"/> <figcaption> <em>Figure 1. Cholesky Algorithm </em> </figcaption> </center></figure>
{: style="text-align: justify"}
 
{: style="text-align: justify"}

{: style="text-align: justify"}
This is the way it needs to be.
{: style="text-align: justify"}

{: style="text-align: justify"}

{: style="text-align: justify"}
{% endraw %}
