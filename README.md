# auto-highlighter
This repo is used for building a sequence-to-sequence model with unique attention mechanism to find salient and representative parts in text.
Find a detailed description on blog here: https://medium.com/p/cbbf333772bf/edit.

## Data Preparation
The CNN/DailyMail dataset will be used for training and evaluating the model.
We will implement the same data preprocessing method as described in (Nallapati et al., 2017).
Code for data preprocessing can be found here: https://github.com/abisee/cnn-dailymail

## Prerequisites
* Pytorch
* Tensorflow
* Python 2 & 3
* [rouge](https://github.com/pltrdy/rouge) 

## Model training
Change the config.py file in the data_util folder for setting hyper-parameter and define file paths.
Run
```
python3 train.py
V

## Model testing
Change the config.py file in the data_util folder for setting hyper-parameter and define file paths.
Run
```
python eval.py --task=test --load_model=[NAME OF YOUR MODEL].tar
```

## References and Credits
* Pointer mechanism for handling Out of Vocabulary (OOV) words [See et al. (2017)](https://arxiv.org/pdf/1704.04368.pdf)
* Intra-temporal and Intra-decoder attention for handling repeated words [Paulus et al. (2018)](https://arxiv.org/pdf/1705.04304.pdf)
* [pointer-generator](https://github.com/abisee/pointer-generator)
* [Text-Summarizer-Pytorch](https://github.com/rohithreddy024/Text-Summarizer-Pytorch/blob/master/README.md)
