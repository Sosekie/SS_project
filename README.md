# SS_project

## Resource:

- Dataset: facebook-faiss: https://github.com/facebookresearch/faiss

- how to use: https://www.pinecone.io/learn/series/faiss/faiss-tutorial/

- Facebook tutorial for LSH: https://www.pinecone.io/learn/series/faiss/

- https://github.com/AlexanderSchultheiss/cherry-harvest/tree/main

- https://www.atlassian.com/git/tutorials/cherry-pick

- https://git-scm.com/docs/git-cherry-pick

## purpose:

- find similar commits
- input: bunchs of commits(include folk)
- output:  clusters of similar commits
- now focus on single repository

## Environment:
- conda create --name  ss
- conda activate ss
- pip install -r requirements.txt
- conda install -c pytorch faiss-gpu

## Question:

1. how k-Shingling deal with long content?

2. for reduce dimension, why not change fc layer's output dimension?

how:

Flat Index：当数据集可以放入RAM并且需要精确搜索时使用。
PQ Index：当内存是考虑因素且数据集较大时，通过Product Quantization压缩向量以减少内存占用。
Flat Index with IVF：对于大型数据集，使用Inverted File System (IVF)可以提高搜索速度。
PQ Index with IVF：同时考虑内存和搜索效率时的选择，尤其是在数据集很大时。
Annoy Index：当向量维度小于100时的选择。
HNSWx Index：当向量维度大于等于100且需要更高效的索引时使用。

Flat Index: Used when the dataset can fit in RAM and an exact search is required.
PQ Index: When memory is a consideration and the dataset is large, compress the vectors with Product Quantization to reduce the memory footprint.
Flat Index with IVF: For large datasets, use Inverted File System (IVF) to improve search speed.
PQ Index with IVF: The choice when considering both memory and search efficiency, especially when the dataset is large.
Annoy Index: the choice when the vector dimension is less than 100.
HNSWx Index: used when the vector dimension is greater than or equal to 100 and a more efficient index is needed.

input and output is fixed

input normalizition

url->commits->diff->similar diff->map commits_brunch_repository

try dr and know, evaluation, ablation of different method

gitlib issues, list of repositories

use cherry harvest, cargo run --release, to test

can use python, push changes to gitlab