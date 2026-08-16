1. Learn how to replicate GPT-2 from scratch
2. BioGPT


| Paper |
|---|
| [GPT-2 (2019): Language Models are Unsupervised Multitask Learners](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)|

* [Reproducing GPT-2 (124M) in llm.c in 90 minutes for $20 #481](https://github.com/karpathy/llm.c/discussions/481)

* HellaSwag Evaluation Metric

***

* 15:00

* 8 H100 GPUs

$$
\begin{align}
\text{Total batch size} &= \text{micro batch size} \times \text{contex window} \times \text{num GPUS} \\
                        &= 64 \times 1,024 \times 8 \\
                        &= 524,288\\
         \text{1-epoch} &= \text{Scan ~complete ~dataset ~once} \\
                        &= \frac{10 ~Billion}{524,200} = 19,073 \\ update steps\\
\end{align}
$$

***

* 30:00

#### Runpod
```
* Pod Name: GPT-2 Replica Build SLM from Scratch
* Edit Template
  * Container Disk - 200
  * Volume Disk - 200 GB
* Change template
  * Runpod PyTorch 2.4.0
* GPU count = 8
* Deploy on Demand
  * Wait!
* Connect -> Jupyter lab -> :888
```

***

* 1:00:00



***


