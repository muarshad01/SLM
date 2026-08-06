

|||
|---|---|
|$d_{model}$|model dimension|
|$n_{heads}$|Number of heads|
|$d_{head}$|Dimension of each head|
|$n_{heads} \times d_{head}$|Embeddign dimension|

***

<p align="center">
  <img src="https://github.com/muarshad01/SLM/blob/main/images/lecture-2/llm-architecture.png" width="500" height="300" />
</p>


#### Transformer Block
1. Layer Norm 1
2. Multi-head Attion (MHA)
3. Dropout
4. Shortcut Connection ($\oplus$)
5. Layer Norm 2
6. Feed forward NN
7. Dropout
8. Shortcut Connection ($\oplus$)

***

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
6. Feed Forward NN (Expansion / Contraction) --> MoE
7. Dropout

***

* __Phase-8__: Going through multiple Transformer block

* __Phase-9__: Normalization layer

* __Phase-10__:

***

