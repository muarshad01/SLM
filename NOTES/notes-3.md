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

* **Note**: 1-epoch is equal to an entire set of batches.

***

* 1:00:00

#### Learning Rate (LR)

$$\theta_{i+1}=\theta_{i}-\alpha\frac{\partial L}{\partial W}$$

* Adam/AdamW

#### Gradient Accumulation
* Batch size = 1,024
* 1 Batch = 32
$\frac{g_1 + g_2 + \ldots + g_{32}}{32}$


#### Hyper Parameters
1. Embedding dimension
2. Vocabulary size
3. Context size
4. Transformer blocks
5. Attention heads
6. FFN - 4 x embedding dimension - 4

***

* 1:10:00 

#### Code

***

* 1:25:00 

***




