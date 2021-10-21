---
layout: page
title: Math Questions
permalink: /paper_reviews/math-test2/
---
<br />
<a name="toc"></a>

<!-- MarkdownTOC depth=4 -->


-  [Open Questions](#open-questions)
    -  [Interpretation of min/max operations](#interpretation-of-min/max-operations)
        -  [What can we do to fix this](#what-can-we-do-to-fix-this)
        -  [Here is a proof that for any function$$f\left( {x,y} \right)$$we have $$\mathop {\max }\limits_y \mathop {\min }\limits_x f\left( {x,y} \right) \le \mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right)$$ ](#here-is-a-proof-that-for-any-function$$f\left(-{x,y}-\right)$$we-have-$$\mathop-{\max-}\limits_y-\mathop-{\min-}\limits_x-f\left(-{x,y}-\right)-\le-\mathop-{\min-}\limits_x-\mathop-{\max-}\limits_y-f\left(-{x,y}-\right)$$-)
-  [Useful General Knowledge](#useful-general-knowledge)
    -  [Use Cholesky to Sample from Gaussian](#use-cholesky-to-sample-from-gaussian)
<!-- /MarkdownTOC -->


<br/>

{% raw %}
<a name="open-questions"></a>

[top](#toc)

<br />

<br />

---
## Open Questions
---

This section contains discussion around open questions I have


<a name="interpretation-of-min/max-operations"></a>

[top](#toc)

<br />

<br />

---
#### Interpretation of min/max operations
---

The repo containing the code for this post is located [here]( https://github.com/chrisnielsen/chrisnielsen.github.io)

A question I have struggled with that is how to interpret the expression:

$$\mathop {\max }\limits_x \mathop {\min }\limits_y f\left( {x,y} \right)$$

So far, I think the best way to interpret this expression is the following: consider breaking the expression into two components as follows:

$$\mathop {\max }\limits_x \mathop {\min }\limits_y f\left( {x,y} \right) = \mathop {\max }\limits_x g\left( x \right)$$ where $$g\left( x \right) = \mathop {\min }\limits_y f\left( {x,y} \right)$$



<a name="what-can-we-do-to-fix-this"></a>

[top](#toc)

<br />

<br />

---
##### What can we do to fix this
---

Therefore, we can interpret this expression as:
1. Pick an x value that we are evaluating
2. Evaluate g(x) for that x value (this will return the y value that minimizes f(x,y) for that choice of x)
3. Repeat step 1 until we find the value of x which maximizes g(x)

Another way to interpret the min/max operations is to think about finding the saddle point of a function. Finding the saddle point is equivalent to finding the min/max solution for a set of variables.


This is a test.



This is a test.


$$\begin{align}
  & \log p\left( x;\theta  \right)=\log \int{p\left( x,z;\theta  \right)\,}dz \\ 
 & \,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,=\sqrt{{{b}^{2}}-4ac} \\ 
 & \,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,=\log \int{p\left( x,z;\theta  \right)\,}dz \\ 
 & \,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,=\log \int{p\left( x,z;\theta  \right)\,}dz \\ 
 & \,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,=\sqrt{{{b}^{2}}-4ac} \\ 
 & \,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,=\log \int{p\left( x,z;\theta  \right)\,}dz \\ 
\end{align}$$ 








<a name="here-is-a-proof-that-for-any-function$$f\left(-{x,y}-\right)$$we-have-$$\mathop-{\max-}\limits_y-\mathop-{\min-}\limits_x-f\left(-{x,y}-\right)-\le-\mathop-{\min-}\limits_x-\mathop-{\max-}\limits_y-f\left(-{x,y}-\right)$$-"></a>

[top](#toc)

<br />

<br />

---
##### Here is a proof that for any function$$f\left( {x,y} \right)$$we have $$\mathop {\max }\limits_y \mathop {\min }\limits_x f\left( {x,y} \right) \le \mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right)$$ 
---


Proof

Suppose that $$\left( {{x^*},{y^*}} \right)$$is the optimal solution to $$\mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right)$$, such that $$\mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right) = f\left( {{x^*},{y^*}} \right)$$. This implies that $$\mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right) = \mathop {\max }\limits_y f\left( {{x^*},y} \right)$$since we can view the inner max operation as being evaluated for a specific x value, and since $${x^*}$$is optimal, we can remove the min operation. 

Now let use examine the situation where the min and max operations are switched such that $$\mathop {\max }\limits_y \mathop {\min }\limits_x f\left( {x,y} \right)$$. Focusing on the inner min operation: since the inner min operation is the minimum over all x values then $$\mathop {\min }\limits_x f\left( {x,y} \right) \le f\left( {{x^*},y} \right)$$.  Since this inequality must hold for all values of y, the inequality is preserved when we take the max operation of y on both sides of the inequality. Therefore, we have that $$\mathop {\max }\limits_y \mathop {\min }\limits_x f\left( {x,y} \right) \le \mathop {\max }\limits_y f\left( {{x^*},y} \right)$$. Now substituting in the expression from above we have:$$\mathop {\max }\limits_y \mathop {\min }\limits_x f\left( {x,y} \right) \le \mathop {\min }\limits_x \mathop {\max }\limits_y f\left( {x,y} \right)$$, 


 **An open question remains regarding when the order of min and max can be exchanged.**


<a name="useful-general-knowledge"></a>

[top](#toc)

<br />

<br />

---
## Useful General Knowledge
---

This section contains general knowledge and tricks about different things that are useful



<a name="use-cholesky-to-sample-from-gaussian"></a>

[top](#toc)

<br />

<br />

---
#### Use Cholesky to Sample from Gaussian
---

There are a number of python functions that can be used to sample from a multivariate Gaussian. One technique is to sample from a standard Gaussian (i.e. zero mean, identity covariance), and then transform the sample such that it resembles being sampled from a Gaussian with mean m and covariance S. This can be achieved as follows (taken from "Gaussian Processes for Machine Learning slide 9")

<figure><center><img src="/assets/img/math-test2/image1.png" alt="Figure 1. Cholesky Algorithm" width="500"/> <figcaption> <em>Figure 1. Cholesky Algorithm </em> </figcaption> </center></figure>
 

This is the way it needs to be.


{% endraw %}
