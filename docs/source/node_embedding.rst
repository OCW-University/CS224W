Node Embedding
==============

.. note::

    Slides: https://web.stanford.edu/class/cs224w/slides/02-nodeemb.pdf

    Colabs: `Colab 0 <https://colab.research.google.com/drive/10-8W1e_WOX4-YocROm8tHbtmn1frUf2S>`_, `Colab 1 <https://colab.research.google.com/drive/1vvIoEqxGl1naopTZbh4bmCOLEiCxvcQq>`_


Graph representation Learning
-----------------------------

What
^^^^

- **Representation learning**: learning the features automatically, a substitute of feature engineering
- **Graph representation learning**: an automatic process to construct *task-independent* features for graphs.

We want to find a universal function :math:`ENC` (called **Encoder**) such that 

.. note::

    For any graph :math:`G=(V, E)` and each node :math:`v\in V`, :math:`ENC(G, v)\in\mathbb{R}^d`. 

And this process is called **node embedding**.



Why
^^^

1. We don't need to design features for every graph.
2. This general-feature-first-fine-tune-second paradigm proves to be very effective.


How
^^^

Node embedding with encoder + decoder framework

1. Define a similarity metric.
2. Use 2 parametic functions, i.e. encoder and decoder, to complete a roundtrip between the vertice set and the embedding space
3. Optimize the parameters such that the inner products in the embedding space approximates the similarity.


Random walk optimization
------------------------

What
^^^^

.. note::
    Optimize embeddings :math:`z_u` to maximize the likelihood of random walk co-occurancies


Algorithm::
    
    1. Run short fixed-length random walks

Why
^^^


How
^^^

- Negative sampling


Node2vec: biased random walk
----------------------------

Other random walk methods
-------------------------

