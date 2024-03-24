# SS_project

问题: "Brute force does not scale" 这意味着，使用暴力搜索（也就是无差别、穷尽所有可能性的搜索方法）来找到某种相似性（这里可能是指代码差异，或者'diff'）不是一个可扩展的方法。在大型数据集上，暴力搜索效率很低，需要非常长的时间，因为随着数据量的增加，所需的计算量呈指数增长。

解决方案: "Approximate nearest neighbor search (k-ANN)" 这是提出的解决方案。k-最近邻（k-NN）是一种用于分类和回归的非参数统计方法。在搜索问题中，这个算法通常被用来查找距离最近的几个邻居。然而，当数据集非常大时，即使是传统的k-NN也会变得效率低下。为了解决这个问题，人们使用了近似最近邻搜索（ANN），这是一个旨在加快最近邻搜索的算法，它牺牲了一定的准确性来换取速度。所以，近似最近邻搜索能够比暴力方法更快地在大型数据集中找到“足够近”的邻居。

向量比较之后进行细节比较（选做）

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

### Environment:
- conda create --name  sspj
- conda activate sspj
- pip install -r requirements.txt
- conda install -c pytorch faiss-gpu


