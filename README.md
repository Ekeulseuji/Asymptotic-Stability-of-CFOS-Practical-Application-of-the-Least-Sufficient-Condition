# Asymptotic-Stability-of-CFOS-Practical-Application-of-the-Least-Sufficient-Condition
A Neural Network-based approach to implement the least sufficient condition for ensuring the Asymptotic Stability of Caputo fractional-order systems

In 2021, study[1] successfully established the least sufficient condition for the Asymptotic Stability of Caputo fractional-order systems:

Suppose $f \in C\left(\mathcal{D}, \, \mathbb{R}^n\right)$ is bounded, with $f(t, 0) \equiv 0$. Suppose there exists a positive definite, continuously differentiable function $V: \mathcal{D} \rightarrow \mathbb{R}$ and a positive definite function $W: \mathcal{D} \rightarrow \mathbb{R}$, such that the Caputo fractional derivative of $W$ and the fractional integral of $W$ both along the solution satisfies the following:

- $V(\textbf{x}) \geq \alpha(\|\textbf{x}\|)$
- $_{t_0}^C {D}^{q}_t \thinspace V(t, \textbf{x}) \leq \thinspace _{t_0}\hspace{-1pt}{I_t}^{1-q}(-W(t, \textbf{x}))$

for all $(t, \textbf{x}) \in \mathcal{D}$, then the trivial solution of the Caputo-type fractional system of order $q$ is AS.

Here, $\thinspace _{t_0} \hspace{-1pt} I_t^{1-q}$ represents the fractional integral of order $1-q$.

 $_{t_0} \hspace{-1pt} I_t^{1-q} = \frac{1}{\Gamma(1-q)} \thinspace \int _{t_0}^{t} \frac{-W(\tau, \textbf{x})}{{(t-\tau)}^{q}} \thinspace \mathrm{d}\tau, \thinspace t_0 \leq \tau \leq t $

where $\Gamma(\cdot)$ is the Gamma function $\Gamma(\gamma) = \int_{0}^{\infty} \psi^{\gamma-1}e^{-\psi} \mathrm{d}\psi$. From equation above, it is evident that the computation of the fractional integral involves the integral over a series of system's solutions $\textbf{x}(\cdot)$ on an unknown positive definite $W$ function at times prior to a certain moment $t$, $\textbf{x}(\tau) \text{ for } t_0 \leq \tau \leq t$, which makes the Least Sufficient Condition challenging to apply in practice. Our proposed method fills the gap in applying the theoretical results to practical systems.

<div align=center>
**Visual Comparisons for the Maximum RoAs Obtained using (a) a widely-used Condition (1); (b) the Least Sufficient Condition (2)**
</div>

<div align=center>
<img src="https://github.com/user-attachments/assets/efa44fd3-00d7-4eee-a15e-b29635ff80ef" width="700" height="320" />
</div>

Results from the illustrative example demonstrate that the proposed method is able to find a valid W which allows Condition (2) to enable a broader range of initial states under which the system can converge. In other words, The larger Region of
Attraction obtained from Condition (2) confirms that this work effectively applies the theoretical least sufficient condition (2) for Asymptotic Stability of Caputo fractional-order systems (originally proposed in 2021 [1]) to the dynamics of practical systems.

[1] C. Wu, “Advances in analysis of caputo fractional-order nonautonomous systems: from stability to global uniform asymptotic stability,” Fractals, vol. 29, no. 04, p. 2150092, 2021.
