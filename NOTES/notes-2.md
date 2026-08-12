## Architecture

<p align="center">
  <img src="https://github.com/muarshad01/SLM/blob/main/images/lecture-2/llm-architecture.png" width="500" height="300" />
</p>

***

#### GPT-2

| GPT-2 ||
|---|---|
| Vocabulary Size     | 50,257 |
| Embedding dimension |    768 |
| Context Window      |  1,024 |
| Transformer Layers  |     12 |

***

#### Token Embedding
* Token embedding matrix = $50,257 \times 768 = 38.6$ Million Parameters

#### Position Embedding
* `The dog chased the cat it couldn't catch it.`
* Position embedding matrix = $1,024 \times 768 = 786,432$ Parameters

#### Input Embedding
* Token Embedding + Position Embedding

***

* 30:00

#### Transformer Block
1. Layer Norm 1 $\bigg(\frac{x_i-\mu}{\sqrt{var}}\bigg)$
2. Multi-head Attention (MHA)
3. Dropout (Randomly set some bits to 0; Helps with generalization; group study project example!)
4. Shortcut Connection ($\oplus$) - alternate path for gradient to flow.
5. Layer Norm 2
6. Feed forward NN - (Expansion, Contraction)
7. Dropout
8. Shortcut Connection ($\oplus$)

***

* 40:00

#### Benefit of Normalization $\bigg(\frac{x_i-\mu}{\sqrt{var}}\bigg)$
* Without normalization: 1) training is not very stable (large or small values); 2) vanishing gradient problem. Gradients become zero and learning stagnates.
* Normalization makes training smoother (stable). In back-propagation, we have a procedure called gradient descent. Normalization 1) makes gradient descent smoother (stable); 2) Prevents vanishing gradient problem

***

* 1:10:00


```
A true friend accepts you
```

* __Phase-1__: Isolation
  * The word is isolated from its neighbors
* __Phase-2__: Token ID assignment
  * Book of Token IDs (Vocabulary)
    * Words
    * Sub-words
    * Characters
  * Byte Pair Encoding (BPE) 
* __Phase-3__: Token embedding assignment

* __Phase-4__: Positional embedding assignment (Your position among neighbors matter!)

```
The dog chased another dog
```

* __Phase-5__: Add token embedding to positional embedding.
  * Input embedding = Token embedding + Positional embedding

* __Phase-6__: Now, you're finally ready to onboard the train to the Transformer block.

***

* __Phase-7__: Different compartments of a Transformer block
1. Layer Norm 1
2. Multi-head Attion --> MLA
3. Dropout (Improves generalization performance; prevents over-fitting)
4. Skip connection or shortcut connnection (help gradient to flow through an alternate path; vanishing gradient problem)
5. Layer Norm 2
6. Feed Forward NN (Expansion / Contraction) --> 768 (IL) + 4x768 (HL) 2x = 
7. Dropout

***

* __Phase-8__: Going through multiple Transformer block

* __Phase-9__: Normalization layer

* __Phase-10__:

***

#### FFNN
* $768 \times (4 \times 768) \times 2 = 4,718,592$ = 4.7 Million x 12 = ~50 Million Parameters

***

