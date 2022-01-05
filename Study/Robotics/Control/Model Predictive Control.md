# Model Predictive Control
#control #prediction #optimization
Model Predictive Control(MPC) is a realization of predictive controls.

Let's say we have a system with state $x\in X$, action $u\in U$, and state transition function $f:X \rightarrow X$ described as follows
$x_t = f(x_{t-1},u_{t-1})$

A MPC considers a optimization problem $\mathcal{P}'(x_t)$ 
$\underset{\symbf{u}_t'}{arg\:min}\:
\sum\limits_{k=1}^{N}\symbf{W}_{sp}(x_{t+k}-sp_{t+k})+
\symbf{W}_{mv}\Delta u_{t+k}$
subject to
$x_t = f(x_{t-1},u_{t-1})$
$\symbf{C} x_{t+k} \leq \symbf{D} \:, k \in \{1,2..,N-1\}$ 
$\symbf{S} u_{t+k} \leq \symbf{T} \:, k \in \{1,2..,N-1\}$

$\symbf{u}_t'$ is a sequence of control inputs $u\in U$ with the size of prediction horizon $N$ consisting of  $\{u_{t},u_{t+1}...+u_{t+N-1}\}$



