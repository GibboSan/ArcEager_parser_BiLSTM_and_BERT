# ArcEager Parser with BiLSTM and BERT-based models

Transition-based dependency parsing is one of the most popular methods for implementing a dependency parsers. 
Here we will implement the static **arc-eager** model, as described in the article ["A Dynamic Oracle for Arc-Eager Dependency Parsing"](https://aclanthology.org/C12-1059/) by Yoav Goldberg and Joakim Nivre.  

As for the dataset we use the huggingface [datasets](https://github.com/huggingface/datasets) library, 
and train on the English `en_lines` [treebank](https://huggingface.co/datasets/viewer/?dataset=universal_dependencies) from the Universal Dependency project. 
It can be easier implemented to work with other languages.

For BERT-tokenizer we use the pre-trained model `"bert-base-multilingual-uncased"`

The notebook will be divided in the following sections:
- Arc-Eager parsing description 
- Dataset Analysis 
- Data set-up
- Baseline model with BiLSTM
- BERT-based model
- Evaluation and Results
- Discussion about SotA in this particular task.

Note that in this work we disregard *arc labels* in dependency trees.

In the notebook it is used the `wandb` library to run results. For a normal run just avoid **wandb's commands** and  fix **hyperparameters configuration**.
