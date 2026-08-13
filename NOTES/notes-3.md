* Part 4: Setting up the SLM training
* Part 5: Pre-training the SLM (GPU training)

***

* 20:00

#### Cross Entropy Loss

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

* Negative log likelihood: $-\frac{1}{4}\big[\log (p_{1}) + \log (p_{2})+\log (p_{3})+\log (p_{4})\big]$
* NOTE: If $p_{1}=p_{2}=p_{3}=p_{4}=1 then Negative log likelihood=0.

***
