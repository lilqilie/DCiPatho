# DCiPatho

DCiPatho is a tool for rapid identification of pathogens from sequencing data. This tool is based on the k-mer frequence data.

## Introduction

Pathogen identification is important for one health perspective. Traditional approaches to open-view pathogen detection depend on databases of known organisms, which limits their performance on unknown, unrecognized, and unmapped sequences. In contrast, machine learning methods can infer pathogenic phenotypes from single NGS reads, even though the biological context is unavailable. We present **DCiPatho**, a deep learning approach to predict the pathogenic potentials of genomic and metagenomic sequences. It is a kind of deep cross neural network. We show that combination of cross, residual and deep neural networks with integrated features of 3-to-7 k-mer outperform on single k-mer features with traditional machine learning approaches. We demonstrate **DCiPatho** model has superior performance in classifying pathogenic bacteria.

## Requirements

DciPatho is developed in Python 3 with modules and external tools.

```
numpy~=1.19.5
torch~=1.10.0+cu102
pandas~=1.1.5
scikit-learn~=0.24.2
```

## **toy dataset**

You can download the k-mer frequencies of mini-RefSeq dataset(toy_dataset_for_DCiPatho.zip) in the link below. Then unzip them to example_data file.

Link：https://drive.google.com/drive/folders/1RsyVqXKy4uyaldfbdmZsRApRc5lcb3wq


## Basic demo for prediction

You can predict pathogenic potentials with the built-in models out of the box, first, change `pred_input_path` in `DCiPatho_config.py` to the directory containing the .fasta file you need to classify, and set `pred_output_path` to the directory where the prediction results need to be output, then:

```
`# run predcit  `

`python DCiPatho.py`
```



## Basic demo for training on mini-RefSeq dataset

You can set the parameter of training and model in DCiPatho_config.py file. Then you can train the DCiPatho model and evaluate it on mini-RefSeq dataset by running:

``````python
`python DCiPatho_main.py`
``````

