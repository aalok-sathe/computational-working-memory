# computational working memory

Perceptual as well internally-generated information is plentiful---being able to use all of this information is essential to optimal planning and decision-making. 
Deciding what information is relevant, choosing to robustly maintain it, accessing it on demand, and overwriting existing information with new, potentially more 
relevant information, are all ecologically-relevant demands that make intelligent behavior possible. 
However, knowing what information is relevant in any given context is difficult and needs to be learned over developmental as well as evolutionary timescales.

This repository serves to enable computational simulations of learning and generalization in service of understanding working memory capacity better. A robustly-engineered 
framework allows researchers to define their own tasks and generate datasets with fine control over the parameters of those tasks. The framework allows for training 
neural models in an architecture-agnostic manner, so long as they support a PyTorch backend. This includes transformers, recurrent neural networks, and long short-term memory
networks that can flexibly act as _participants_ in the same tasks, allowing for clean, controlled comparisons across model instantiations.

Integration with the 
[weights & biases (`wandb`)](https://wandb.ai)
experiment-tracking platform promotes robust, open, and replicable science by constructing uniquely-tagged and documented config-driven experiments for each condition
a researcher may be interested in. These experimental conditions live in separate spaces on the disk, each with meticulously documented metadata that makes
discerning results and analyzing data pleasantly organized. Furthermore, the software supports exposure and transfer-learning experiments using these same condition-based
tags, allowing precise documentation of the entire training history of a computational model and subsequent experiments on pretrained models.

The main module (`-m workingmem`), implemented with an entrypoint in `workingmem/__main__.py` does the orchestrating of loading/constructing datasets, training/evaluating models.
To see the options, run `python -m workingmem -h`.
