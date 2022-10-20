### Multiple Lin Reg 
- Polynomial basis function: $\phi(x_i) = \left[1, x_i, x_i^2, \dots, x_i^M\right]^T, \forall i$
- Mapper: $y = f(\phi(x),\mathbf{w}) = \sum_{j=0}^{M} w_j\phi_j(x) = f(\phi(x),\mathbf{w}) = \mathbf{X}\mathbf{w}$
- Linear Regression Objective Function (Mean squared error): $J(\mathbf{w}) = \frac{1}{2} \sum_{n=1}^N \left(t_n - f(\phi(x_n),\mathbf{w})\right)^2 = \frac{1}{2}\left\Vert \mathbf{t} - \mathbf{X}\mathbf{w} \right\Vert^2_2$
- Solution:  $\mathbf{w} =(\mathbf{X}^T\mathbf{X})^{-1}\mathbf{X}^T\mathbf{t}$

### Regularization
- Ridge Regularizer: $R^{(L2)}_{\mathbf{w}} = \lambda \sum_{i=0}^M w_i^2 = \lambda \Vert\mathbf{w}\Vert_2^2$
- Lasso Regularizer: $R^{(L1)}_{\mathbf{w}} = \lambda \sum_{i=0}^M |w_i| = \lambda \Vert\mathbf{w}\Vert_1$
- Elastic Net Regularizer: $R^{(L12)}_{\mathbf{w}} = \beta\lambda \sum_{i=0}^M |w_i| + (1-\beta) \lambda \sum_{i=0}^M w_i^2 = \beta R^{(L1)}_{\mathbf{w}} + (1-\beta) R^{(L2)}_{\mathbf{w}}$

### Logistic Regression (Logit)
- Mapper: $y = \phi(z) = \frac{1}{1+\exp(-z)}$ where $z = \mathbf{w}^Tx+w_0$
- Activation function: $\hat{t} = \begin{cases}1,  z\geq 0\\ 0,  z<0\end{cases}  = \begin{cases}1,  \mathbf{w}^Tx+w_0\geq 0\\ 0,  \mathbf{w}^Tx+w_0<0\end{cases}$
- Logistic Regression Objective Function: $J(\mathbf{w},w_0) = \sum_{i=1}^N - t_i\log\phi(z_i) - (1-t_i)\log(1-\phi(z_i))$
- With regularizer (see Regularization): $J(\mathbf{w}, w_0) + R$

### Performance Measures of Classification Tasks
- $\begin{align*} \text{accuracy} = \frac{N_{\text{corr}}}{N} \end{align*}$
- $\begin{align*} \text{error} = \frac{N_{\text{miss}}}{N} \end{align*}$

#### Precision, recall, fall-out
- Positive Predictive Value: $\begin{align*} \text{Precision} = \text{PPV} = \frac{TP}{TP + FP} \end{align*}$
- True Positive Rate: $\begin{align*} \text{Recall} = \text{TPR} = \text{Sensitivity} = \frac{TP}{TP + FN} \end{align*}$
- False Positive Rate: $\begin{align*} \text{Fall-out} = \text{FPR} = \frac{FP}{FP + TN} \end{align*}$
- True Negative Rate: $\begin{align*} \text{Specificity} = \frac{TN}{TN + FP} \end{align*}$
- F-Score, F-measure: $\begin{align*} \text{F1-score} = \frac{2}{\frac{1}{\text{Precision}} + \frac{1}{\text{Recall}}} = 2\times\frac{\text{Precision}\times \text{Recall}}{\text{Precision} + \text{Recall}} \end{align*}$




#### Softmax regression
- Single K-class discriminant of the form: $\begin{align*} y_k(\mathbf{x}) = \phi(\mathbf{w}_k^T\mathbf{x} + b_k) \end{align*}$
- D-1 dimensional hyperplane: $\begin{align*} (\mathbf{w}_k - \mathbf{w}_j)^T\mathbf{x} + (b_k - bj) = 0 \end{align*}$
- Softmax function: $\begin{align*} p_k = \frac{\exp(y_k(\mathbf{x}))}{\sum_{j=1}^K \exp(y_j(\mathbf{x}))} \end{align*}$ 

### Decision Trees, Random Forests
- Entropy: $I_H = -\sum_{j=1}^c p_j \log_2(p_j)$
- Gini index: $I_G = 1 - \sum_{j=1}^c p_j^2$
- Classification error: $I_E = 1 - \max_{j=1,\dots,c}(p_j)$
- Binary split Information Gain: $IG(D_p, f) = I(D_p) - \frac{N_{\text{left}}}{N_p} I(D_{\text{left}}) - \frac{N_{\text{right}}}{N_p} I(D_{\text{right}})$

### Ensemble Learning, Bagging & Boosting
- Weight assessment: $\begin{align*} r_j = \frac{\sum\limits_{\substack{i=1 \\ \hat{y}_j^{(i)}\neq y^{(i)}}}^N w^{(i)}}{\sum_{i=1}^N w^{(i)}} \end{align*}$

- Predictor’s weight: $\begin{align*} \alpha_j = \eta \log\frac{1-r_j}{r_j} \end{align*}$
- Predicted class: $\begin{align*} \hat{y}(x) = \arg_k\max \sum\limits_{\substack{j=1 \\ \hat{y}_j(x)=k}}^M \alpha_j \end{align*}$

### Hard/Soft SVMs 
Kernel machine
- Kernel function: $\begin{align*} k: \mathbb{R}^d \times \mathbb{R}^d &\longrightarrow \mathbb{R}\\ (\mathbf{x},\mathbf{y})&\longmapsto k(\mathbf{x},\mathbf{y})=\phi(\mathbf{x})^T\phi(\mathbf{y}) \end{align*}$
- Phi = fixed nonlinear feature space mapping: $\begin{align*} \phi: \mathbb{R}^d &\longrightarrow \mathbb{R^D}\\ \mathbf{x}&\longmapsto \phi(\mathbf{x}) \end{align*}$
- Radial Basis Function (RBF Kernel): $\begin{align*} k_{\text{RBF}}(\mathbf{x},\mathbf{y}) &= \exp\left(-\gamma\Vert\mathbf{x}-\mathbf{y}\Vert^2\right) \end{align*}$
- Typical values for gamma: $\gamma=\frac{1}{2\sigma^2}$
- Support Vector Machine
- Design a hyperplane: $y(x) = w^T\phi(x) + b = 0$
