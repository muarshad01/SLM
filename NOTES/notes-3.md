* Part 4: Setting up the SLM training
* Part 5: Pre-training the SLM (GPU training)

***

* 20:00

#### Cross Entropy Loss

<p align="center">
  <img src="https://github.com/muarshad01/SLM/blob/main/images/lecture-3/NLL.png" width="500" height="300" />
</p>

$$
P = \left[
    \begin{array}{@{}c@{}}
       p_{1} \\
       p_{2} \\
       p_{3} \\
       p_{4} \\
    \end{array} 
\right]
$$

* Negative log likelihood: $-\frac{1}{4}\big[\log (p_{1}) + \log (p_{2})+\log (p_{3})+\log (p_{4})\big]=-\frac{1}{4}\big[\log (p_{1}\times p_{2} \times p_{3} \times p_{4})\big]$
* **NOTE**: If $p_{1}=p_{2}=p_{3}=p_{4}=1$ then Negative log likelihood=0.
* Loss for one input sequence
* Loss for one batch

***

* 30:00

#### Forward Pass
* Batch -> SLM -> Predict NextToken -> Loss

#### Batch Gradient Descent
$$Loss(L) = f(p_1,p_2, \ldots, p_{100M})$$

$$\frac{\partial L}{\partial p_1};\frac{\partial L}{\partial p_2};\ldots;\frac{\partial L}{\partial p_{100M}}.$$

#### Update Rule - ADAM
$$
\begin{align}
  p_1 &= p_1-\alpha\frac{\partial L}{\partial p_1}\\
  p_2 &= p_2-\alpha\frac{\partial L}{\partial p_2} \\
  \ldots\\
  p_{100M} &= p_{100M}-\alpha\frac{\partial L}{\partial p_{100M}};\\
\end{align}
$$

***


