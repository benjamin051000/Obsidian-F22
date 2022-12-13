### Hard/Soft SVMs 
Kernel machine
- Kernel function: $\begin{align*} k: \mathbb{R}^d \times \mathbb{R}^d &\longrightarrow \mathbb{R}\\ (\mathbf{x},\mathbf{y})&\longmapsto k(\mathbf{x},\mathbf{y})=\phi(\mathbf{x})^T\phi(\mathbf{y}) \end{align*}$
- Phi = fixed nonlinear feature space mapping: $\begin{align*} \phi: \mathbb{R}^d &\longrightarrow \mathbb{R^D}\\ \mathbf{x}&\longmapsto \phi(\mathbf{x}) \end{align*}$
- Radial Basis Function (RBF Kernel): $\begin{align*} k_{\text{RBF}}(\mathbf{x},\mathbf{y}) &= \exp\left(-\gamma\Vert\mathbf{x}-\mathbf{y}\Vert^2\right) \end{align*}$
- Typical values for gamma: $\gamma=\frac{1}{2\sigma^2}$
- Support Vector Machine
- Design a hyperplane: $y(x) = w^T\phi(x) + b = 0$
### Princpal Component Analysis (PCA)
- $\mathbf{X}$: original data
- $\mathbf{A}$: n-top eigenvectors
- $\mathbf{Y}$: Transformed data that maximizes variance
- $\mathbf{Y}=\mathbf{A}\mathbf{X}$
- Recovery:  $\mathbf{\hat{X}}=\mathbf{A^\dagger}\mathbf{Y}$
### Clustering
- Silhouette index: $s=\frac{1}{N}\sum_{i=1}^{N}\frac{b_i-a_i}{max(a_i,b_i)}$
- Rand index: $r=\frac{a+b}{a+b+c+d}$
### Perceptron
- Perceptron criterion: $E_p(\mathbf{w},b)=-\sum_{n\in M}(\mathbf{w}^T\mathbf{x}_n+b)t_n$
