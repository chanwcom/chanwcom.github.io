---
title: "Sentence Piece Tutorial"
categories:
  - Tutorials
tags:
  - minimal mistakes
  - jekyll
  - blog
  - standard
toc: true
toc_sticky: true
toc_label: "GITHUB BLOG START"
toc_icon: "blog"
---

# Introduction

# Preparation

## Installation of SentencePiece


 *SentencePiece* is a toolkit for sub-word tokenization. In this tutorial, we assume that you are using Ubuntu Linux.
 [Link to the *SentencePiece* github page](https://github.com/google/sentencepiece)

 ```
 conda config --add channels conda-forge
 conda config --set channel_priority strict
 ```

 ```
 conda install libsentencepiece sentencepiece sentencepiece-python sentencepiece-spm
 ```

 or 

 ```
 pip install sentencepiece
 ```



## STOP data set

In this tutorial, we will use the STOP dataset. Information about this dataset may be found at the following link:
https://facebookresearch.github.io/spoken_task_oriented_parsing/
Stop dataset was developed for benchmarking the Spoken Language Understanding (SLU) task.

You may download it from the following link:
[Link to the download page](https://github.com/facebookresearch/fairseq/tree/main/examples/audio_nlp/nlu)


# Algorithm


# Running it


```
spm_train --input=train-all.trans_without_uttid.txt \
       --model_prefix=model_unigram_256  \
       --vocab_size=256 \
       --character_coverage=1.0 \
       --model_type=unigram
```


# Doing tokenization and detokenization


# Summary



In this page, we discuss how to define a model using Keras.
