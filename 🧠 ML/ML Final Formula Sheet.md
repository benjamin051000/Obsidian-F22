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
- Activation Functions:
	1. **Heaviside Step:** $\phi(x) = \begin{cases}1, & x >0 \\ 0, & x\leq 0\end{cases}$
	2. **Linear:** $\phi(x) = x$
	
	3. **Sigmoid:** $\phi(x) = \frac{1}{1+e^{-x}}$
	
	4. **Hyperbolic Tangent (tanh):** $\phi(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}$
	
	5. **Rectified Linear Unit (ReLU):** $\phi(x) = \begin{cases} x, & x> 0 \\ 0, & x \leq 0\end{cases}$
	
	6. **Leaky ReLu:** $\phi(x) = \begin{cases} x, & x> 0 \\ 0.01x, & x \leq 0\end{cases}$
	
	7. **Exponential Linear Unit (ELU):** $\phi(x) = \begin{cases} x, & x> 0 \\ \alpha (e^x -1), & x \leq 0\end{cases}$
	where $\alpha=1.67326$.
	
	8. **Scaled Exponential Linear Unit (SELU):** $\phi(x) = \lambda\begin{cases} x, & x> 0 \\ \alpha (e^x -1), & x \leq 0\end{cases}$
	where $\alpha=1.67326$ and $\lambda=1.0507$.
	
	9. **Softplus:** $\phi(x) = \ln(1+e^x)$
	
- Objective Function: $J(w)=\frac{1}{2}\sum_{k=1}^N(t_k-w^Tx_k)^2$
- 
| Activation function | $\phi(x)$ | $\phi'(x) = \frac{d\phi(x)}{dx}$ |
| -- | -- | -- |
| Linear | $x$ | $1$ |
| Sigmoid/Logistic | $\frac{1}{1+e^{-x}}$ | $\phi(x)(1-\phi(x))$ |
| Tanh | $\frac{e^{x}-e^{-x}}{e^x + e^{-x}}$ | $1-\phi(x)^2$ |
| ReLU | $\begin{cases}0, & x \leq 0 \\ x, & x>0 \end{cases}$ | $\begin{cases}0, & x < 0 \\ 1, & x>0 \\ \text{undefined}, & x=0\end{cases}$ |
| Leaky ReLU | $\begin{cases}0.01 x, & x \leq 0 \\ x, & x>0 \end{cases}$ | $\begin{cases}0.01, & x < 0 \\ 1, & x>0 \\ \text{undefined}, & x=0\end{cases}$ |
| Softplus | $(1+e^x)$ | $\frac{1}{1+e^{-x}}$ |
| ELU | $\begin{cases}\alpha(e^x-1), & x \leq 0 \\ x, & x>0 \end{cases}$ |  $\begin{cases}\alpha e^x, & x < 0 \\ 1, & x>0 \\ 1, & x>0 \text{ and } \alpha=1  \end{cases}$ |
| SELU | $\lambda\begin{cases}\alpha(e^x-1), & x < 0 \\ x, & x\geq 0 \end{cases}$ | $\lambda\begin{cases}\alpha e^x, & x < 0 \\ 1, & x\geq 0 \end{cases}$ |
- Updating weights
	- Output: $v_j=w^Tx_j$
	- Gradient: $\delta_j=\phi'(v_j)\sum_t\delta_lw_{lj}$
	- Weight update eqns:
		- $\Delta w_{ij}=\eta\delta_jx_i$ 
		- $w_{ij}^{(t+1)}\leftarrow w_{ij}^t+\Delta w_{ij}^t$	

- CNN total parameters: $\sum$ parameters per layer
- CNN # Parameters per layer: (Kernel size * # input feature maps + 1 (bias) ) * # output feature maps
- Memory usage per layer: (pixel width * pixel height / stride^2 * # feature maps + CNN total params) * `sizeof(float)` 
- Entire mem usage (*optimized*): $\sum$ Largest 2 layers
- Mini-batches: Entire mem usage (*unoptimized*) * # batches
