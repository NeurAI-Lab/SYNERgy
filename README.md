# SYNERgy 
Official Repository for CoLLAs 2022 paper "[SYNERgy between SYNaptic consolidation and Experience Replay for general continual learning](https://arxiv.org/pdf/2206.04016.pdf)".

We extended the [CLS-ER](https://github.com/NeurAI-Lab/CLS-ER) repo with our method (SYNERgy).

## Setup

+ Use `python main.py` to run experiments.
+ Use argument --load_best_args to use the best hyperparameters for each of the evaluation setting from the paper.
+ To reproduce the results for SYNERgy in the paper run the following
    `python main.py --dataset <dataset> --model synergy --buffer_size <buffer_size> --load_best_args`

 Examples:

    python main.py --dataset rot-mnist --model synergy --buffer_size 500 --load_best_args
    
    python main.py --dataset seq-cifar10 --model synergy --buffer_size 500 --load_best_args
    
    python main.py --dataset seq-tinyimg --model synergy --buffer_size 500 --load_best_args

    python main.py --dataset gcil-cifar100 --weight_dist unif --model synergy --load_best_args
    
    python main.py --dataset gcil-cifar100 --weight_dist longtail --model synergy --load_best_args
    

## Requirements

- torch==1.7.0

- torchvision==0.9.0 

- quadprog==0.1.7

## Cite Our Work

If you find the code useful in your research, please consider citing our paper:

    
   @InProceedings{pmlr-v199-sarfraz22a,
  title = 	 {SYNERgy between SYNaptic Consolidation and Experience Replay for General Continual Learning},
  author =       {Sarfraz, Fahad and Arani, Elahe and Zonooz, Bahram},
  booktitle = 	 {Proceedings of The 1st Conference on Lifelong Learning Agents},
  pages = 	 {920--936},
  year = 	 {2022},
  editor = 	 {Chandar, Sarath and Pascanu, Razvan and Precup, Doina},
  volume = 	 {199},
  series = 	 {Proceedings of Machine Learning Research},
  month = 	 {22--24 Aug},
  publisher =    {PMLR},
  pdf = 	 {https://proceedings.mlr.press/v199/sarfraz22a/sarfraz22a.pdf},
  url = 	 {https://proceedings.mlr.press/v199/sarfraz22a.html},
  abstract = 	 {Continual learning (CL) in the brain is facilitated by a complex set of mechanisms. This includes the interplay of multiple memory systems for consolidating information as posited by the complementary learning systems (CLS) theory and synaptic consolidation for protecting the acquired knowledge from erasure. Therefore, we propose a general CL method that creates a synergy between SYNaptic consolidation and dual memory Experience Replay (SYNERgy). Our method maintains a semantic memory that accumulates and consolidates information across the tasks and interacts with the episodic memory for effective replay. It further employs synaptic consolidation by tracking the importance of parameters during the training trajectory and anchoring them to the consolidated parameters in the semantic memory. To the best of our knowledge, our study is the first to employ dual memory experience replay and synaptic consolidation in conjunction which is suitable for general CL whereby the network does not utilize task boundaries or task labels during training or inference. Our extensive evaluation on various challenging CL scenarios and characteristics analyzes demonstrate the efficacy of incorporating both synaptic consolidation and CLS theory in enabling effective CL in DNNs.}
}

