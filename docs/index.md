# Welcome to MkDocs

For full documentation visit [mkdocs.org](http://mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs help` - Print this help message.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

Hypothesis:         $h_\theta(x)=\theta^Tx=\theta_0x_0+\theta_1x_1+\theta_2x_2+...+\theta_nx_n$

Parameters:         $\theta_0,\theta_1,...,\theta_n$

Cost function:   
$$
J(\theta_0,\theta_1,...,\theta_n)=\frac {1} {2m}\sum\limits_{i=1}^{m}(h_\theta(x^{(i)})-y^{(i)})^2
$$
Gradient descent:
Repeat{
$$
\theta_j :=\theta_j-\alpha\frac{\partial}{\partial \theta_j}J(\theta_0,\theta_1,...,\theta_n)
$$
​	     }（simultaneously update for every j=0, 1, 2, ..., n)）

推导一： $\frac{\partial}{\partial \theta_j}J(\theta_0,\theta_1,...,\theta_n)=?$

Let's first work it for the case if we have only one training example $(x,y)$, so that we can neglect the sum in the definition $J$. We have:
$$
\begin{aligned} 
\frac{\partial}{\partial \theta_j}J(\theta_0,\theta_1,...,\theta_n)&=
\frac {1} {2}\frac{\partial}{\partial \theta_j}(h_\theta(x)-y)^2\\
&=2\cdot\frac{1}{2}\cdot(h_\theta(x)-y)\cdot\frac{\partial}{\partial \theta_j}(h_\theta(x)-y)\\
&=(h_\theta(x)-y)\cdot\frac{\partial}{\partial \theta_j}(\theta_0x_0+\theta_1x_1+\theta_2x_2+...+\theta_nx_n)\\
&=(h_\theta(x)-y)\cdot x_j
\end{aligned}
$$



