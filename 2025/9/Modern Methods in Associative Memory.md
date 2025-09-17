#### table of contends

🔗[paper link](https://arxiv.org/abs/2507.06211)


# Abstract and Conclusion

Hopfield + SOTA

# Introduction

Associate memory + Dense Associate Memory

# Dense Associate Memory

- energy function $F$ and Local activation function $f$
- Capacity




# General Dense Associative Memory
- Limit and solution
- The dual energy $E_x(x)$ has another nice property: its gradient equals the hidden states.
- 

| Architectur | ET| Transformer |
|----------|----------|----------|
| Layer Norm    |  ensure energy-based dynamics are well-behaved | Stabilize traning     |
|     |  Balances the contribution of Hopfield and attention so that the global energy is still bouded   | Mostly about numerical conditioning of residual connections   |
| Multi-head| exchange information between tokens| 
|| don't have value matrix but has a function||
| Aspect | Parallel | Sequential |
|Hopfield block|similar to MLP but the the weights of the projection should be the smae|
| Hopfield Network Module | HN model is an MLP with shared weights that is applied recurrently | MLP|

# Failure of Memory and Generative of AI
| Architecture| HF| Diffusion|
|--------|----------------|-----------------|
|Loss function/Energy| $$ E = - \sum _{\mu = 1}^{K} F(\sum _{i=1}^D \xi _i ^{\mu} \sigma_i)$$|$$\nabla _{\mathbf{x}_t} \log p_t(\mathbf{x}_t) = - \nabla_{\mathbf{x}_t} E_{\theta}(\mathbf{x}_t, t)$$|
Behave| recurently lower the energy function | during training, leanr how to remove noise from a perturbed memory to obtain a clean memory|
| Fixed Point| fixed points must be the same | fixed points must be the same|

# Associative Memory: A Machine learning model

## 5.1

Build relaitonship between machine learning and HP

## 5.2 Associatvie memory network as a Model

why build the relationship between energy function and probability using Boltzmann distribution?
$p(v) = \frac {1} {Z} e^ {-E(v)}$

### parametric Models

Associate memory network can generalize
- Enough data, which smooths hte energy landscape naturally
- Parametric training with a loss, which enforces generalizable attractors

# 5.3 Cluster
- classic clustering
- continuous clustering
- enumerate form
- Voronoi partition

Deep cluster
- normal
- reconstruction
- internal structure



## 5.4.1 Random Features

why introduce 5.29

why should we use trigonometric functions

- RBF (radial basis function) kernel(unpractical -> random Fourier transform)
- prperties

# novel genelization

- energy function -> kernel density estimate
- 