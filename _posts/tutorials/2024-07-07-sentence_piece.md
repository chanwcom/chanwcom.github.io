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

## Installation of Sentence Piece


 Sentence Piece is a toolkit for tokenization. You may install it on Ubuntu environment.

 ```
 conda config --add channels conda-forge
 conda config --set channel_priority strict
 ```




## STOP data set

In this example, we will use the STOP dataset.


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
