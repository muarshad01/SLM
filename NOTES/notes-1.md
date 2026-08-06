* [Colab Paid Services Pricing](https://colab.research.google.com/signup)

* **Part 1**: Dataset
* **Part 2**: Data pre-processing (Tokenization; Input/Output pairs)
* **Part 3**: Assembling the model architecture
* **Part 4**: Setting up the SLM training
* **Part 5**: Pre-training the SLM (GPU training)
* **Part 6**: Running Inference

**** 

* 10:00

* Statistical (probabilistic) prediction of next word
* What if I made a model which estimates the probabilities with which the next word can appear?

***

* 20:00

<p align="center">
  <img src="https://github.com/muarshad01/SLM/blob/main/images/lecture-1/model-accuracy.png" width="500" height="300" />
</p>p


* Emergent Behavior
* Model learns form and meaning of language

***

* 40:00

#### Part-1: Our Dataset

| Paper |
|---|
| [TinyStories: How Small Can Language Models Be and Still Speak Coherent English?](https://arxiv.org/abs/2305.07759) |

* [TinyStories Datasets at Hugging Face](https://huggingface.co/datasets/roneneldan/TinyStories)


***

* 50:00

#### Part 2: Data pre-processing (Tokenization; Input/Output pairs)
* Word based tokenization
  * Issues: computational time; spelling mistakes (**OOV problem** - i.e., out of vocabulary problem); 
* Character based tokenization
  * Issues: We loose the essence of English language; **context-window problem**
* Sub-word based tokenization
  * [Understanding Byte Pair Encoding (BPE) in Large Language Models](https://vizuara.substack.com/p/understanding-byte-pair-encoding)
  * [The necessary (and neglected) evil of Large Language Models: Tokenization](https://vizuara.substack.com/p/the-necessary-and-neglected-evil)
  * It solves OOV problem; reduces vocab size; preserves essence of language

***

* [Tiktokenizer App](https://tiktokenizer.vercel.app/)
* GPT-2 vocab-size is $50,527$.

***

* 1:20:00

* Train.bin
* Validation.bin

***

#### Create Input-Output Pairs from Dataset
* (batch-size, context-size) = (4, 4)
* Context Window (Number of tokens the model looks at one time!)
* Batch Size
* GPT-2 context-size is $1,024$

***

* LLM are Autoregressive & Self-Supervise

***

* 1:40:00

***




