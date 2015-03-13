---

title: Perceptron
layout: default
categories: [Machine Learning]
tags: [Machine Learning, Perceptron, Online Learning]

---

### Introduction

Perceptron is to learn a linear function $f(w, x)=w^Tx+b$.
Each $w$ corresponds to one hypothesis $h(x)=sign(f(w, x))$.
A prediction is correct if $y*(w^Tx)>0$.
Goal of learning is to find a good $w$ such that $h(x)$ makes few mis-predictions.

### Loss Functions
![](http://i.imgur.com/ZKdcgTQ.png)
![](http://i.imgur.com/BOiDe9m.png)

### Update
Use stochastic gradient descent to solve the loss functions.
$$
\mathcal J(\mathbf w)=\frac{1}{N}\sum_{i=1}^N \max(0,  -y_i\mathbf w^T \mathbf x_i) 
\\
\mathcal J_i(\mathbf w)=max(0,  -y_i\mathbf w^T\mathbf x_i) 
\\
 \frac{\partial \mathcal J_i}{\partial w_j} = 
 \begin{cases}
0,  & \text{if $y_i\mathbf w^T\mathbf x_i>0$} \\
-y_ix_{ij}, & \text{otherwise}
\end{cases} 
\\ 
\begin{cases}
0,  & \text{if $y_i\mathbf w^T\mathbf x_i>0$} \\
-y_i\mathbf x_i, & \text{otherwise}
\end{cases}
$$

so we get the update rule:

$$ 
\mathbf w = \mathbf w + y_i\mathbf x_i,   \;\text{if it is a mistake} 
$$

### Intuition
![](http://i.imgur.com/TlexcYV.png)

### Algorithms

![](http://i.imgur.com/bvWrQ1o.png)


### Convergence
![](http://i.imgur.com/LCQFBFE.png)
![](http://i.imgur.com/m7JV4aF.png)
![](http://i.imgur.com/GQVzmgC.png)