## Architecture

<p align="center">
  <img src="https://github.com/muarshad01/SLM/blob/main/images/lecture-2/llm-architecture.png" width="500" height="300" />
</p>

***

#### Transformer Block
1. Layer Norm 1
2. Multi-head Attention (MHA)
3. Dropout (Randomly set some bits to 0; Improves generalization performance; prevents over-fitting; Group study project example!)
4. Shortcut Connection ($\oplus$) - helps gradient to flow through an alternate path; vanishing gradient problem!
5. Layer Norm 2
6. Feed forward NN - (Expansion, Contraction)
7. Dropout
8. Shortcut Connection ($\oplus$)

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
* Input embedding = Token embedding + Positional embedding

***

* 40:00

#### Layer Normalization
* [Layer Normalization](https://github.com/muarshad01/LLM/blob/main/Notes/lecture20_notes.md)

***

* 1:10:00

#### Attention
* [Attention](https://github.com/muarshad01/DeepSeek/blob/main/Notes/lecture05_notes.md)

***

* 1:30:00

#### MHA - Perspectives
* The artist painted the portrait of a woman with a brush.
1. painting a woman with a "brush"
2. painting of a "woman with a brush"

***

* 1:40:00

#### Output Projection Matrix W_0
* $W_0(768,50,257)$
* $(4, 50,257) = (4,768) \times (768,50,257)$

***

* 1:50:00

***

#### FFNN
* $768 \times (4 \times 768) \times 2 = 4,718,592$ = 4.7 Million x 12 = ~50 Million Parameters

***



