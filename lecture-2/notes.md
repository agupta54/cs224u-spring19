# Distributed Word Representations 

Meaning is latent in co-occurence

## High-level goals

### Matrix Designs

* Begin thinking about how vwctos can encode the meanings of linguistic units.

* Foundational concepts of vector space models (VSMs).

| Matrix design | Reweighting | Dimensionality Reduction | Vector Comparison |
|---|----|----|---|
|word x document| probabilities| LSA | Eucledian |
|word x word| length norm | PLSA | Cosine |
|word x search proximity | TF-IDF| LDA | Dice |
|adj. x modified noun| PMI | PCA | Jaccard |
|word x dependency rel. | Positive PMI | NNMF | KL |

We are taking a real world pbject and representing them as handcrafted features.

### Vector Comparisons

#### **Eucledian**

*eucledian(u,v)* = $\sqrt{\sum_{i=1}^n |u_i - v_i|^2}$

#### **Cosine Distance** 

Between vectors u and v of dimension n:

*cosine(u,v)* = 1 - $\dfrac{\sum_{i=1}^n u_i \times v_i}{||u||_2 \times ||v||_2}$

## KL Divergence 

Between probability distributions p and q:

$D(p||q) = \Sigma_{i=1}^n p_ilog(\frac{p_i}{q_i})$

$p$ is the reference distribution. Before calculation, smooth by adding $\epsilon$.
This is not syymetric
