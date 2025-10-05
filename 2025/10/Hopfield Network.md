# Hopfield Network

📕 [paper link](https://pmc.ncbi.nlm.nih.gov/articles/PMC346238/)

Hopfield Network is a information storage system which have 3 functions:
1. (Write)Store information

2. (Read)Retrive Information

3. (State evolution)


The instaneous state of the system is a Vector $V = (V_1, V_2, V_3, ...)$, for each $V_i \in V$ is a neuron with 2 states $V_i \in \{0, 1\}$. The neuron i adjust its state follow the rule below: 

$$
V_i \to 
\begin{cases}
1, & \text{if } \displaystyle\sum_{j \ne i} T_{ij} V_j > U_i, \\\\[8pt]
0, & \text{if } \displaystyle\sum_{j \ne i} T_{ij} V_j < U_i.
\end{cases}
$$
## Write Function
We build the storaged patterns $V^s: s \in {1,2,...,n}$. We build the strength of connection $T_{ij}$, following this prescription $T_{ij} = \sum _s (2 V_i ^s -1)(2 V_j ^s  - 1)$ with $T_{ii} = 0$ st $s' \in s$, $V_i ^{s'}$ is stable and correspond to $V_i ^{s'}$.

Learning Algorithm to learn matrice $T_{ij}$. 

$$
\Delta T_{ij} = [V_i(t) V_j(t)]_{average}
$$

Let's discuss how does the initial stored synaptic strength envolve to the final stroed synaptic strength.

We have $\Delta T_{ij} = [V_i(t) V_j(t)]_{average}$, so $T_{ij}$ is not fixed - it's gradually built by summing many small updates over time, thus we get $T_{ij} = \sum _t \Delta T_{ij} (t)$


When the network is exposed to a specific pattern $V^s$, we get $\Delta T_{ij}^{(s)} = [V^s_iV^s_j]_{average}$. Finally we get $T_{ij} = \sum _{s=1} ^n \Delta T_{ij} ^s = \sum _{s=1} ^n [V_i^s V_j^s]_{average}$

