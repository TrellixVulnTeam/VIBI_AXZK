<h1 align="center">
    VIBI: Explaining a black-box using Deep Variational Information Bottleneck Approach
</h1>

<br>

## Overview
This repo includes pytorch implementation of **VIBI**. VIBI is a system-agnostic interpretable machine learning method that provides a brief but comprehensive explanation. It adopts the inspring information theoretic principle, *information bottleneck principle*. Using an information theoretic objective, VIBI selects instance-wise key features that are maximally compressed about an input (briefness), and informative about a decision made by a black-box on that input (comprehensive). The selected key features act as an information bottleneck that serves as a concise explanation for a black-box decision. Please see our recent paper -- [arXiv preprint](https://arxiv.org/abs/1902.06918).

<img src="img/aim3-overview.pdf" width="100">
<img src="img/aim3-imdbmnist.pdf" width="100">
[![Figure 1. Overview of VIBI](img/aim3-overview.pdf)](img/aim3-overview.pdf)
[![Figure 2. Explanations provided by VIBI](img/aim3-imdbmnist.pdf)](img/aim3-imdbmnist.pdf)

## Usage
Download and install the environment from Cloud.
```
conda env create SeojinBang/py36
conda activate py36
```

See main.py for possible arguments.

To learn a black-box model for MNIST digit recognition:
```
python mnist/original.py --model_type cnn --model_name original.ckpt --epoch 5
```

To learn VIBI to explain the black-box model:
```
python main.py --dataset mnist --epoch 40 --beta 0.1 --K 4 --explainer_type cnn4 --chunk_size 4 --mode train
```

<br>

## Credit
[DeepVIB Repo](https://github.com/1Konny/VIB-pytorch): pytorch implementation of deep variational information bottleneck. 

## References
Bang et al. 2019. **Explaining a black-box using Deep Variational Information Bottleneck Approach.** *ArXiv Preprint* [arXiv:1902.06918v1](https://arxiv.org/abs/1902.06918).

## Contact
Please feel free to contact me by e-mail `seojinb at cs dot cmu dot edu`, if you have any questions.

