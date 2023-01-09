Has a fudge-factor that softens the requirements of the Hard-Margin SVM.

- Promotes generalization and reduces [[Overfitting]] by allowing points to be misclassified or enter the margin.
- Such points will be penalized by using a slack variable.

# Slack Variable
- $\mathcal{E}_n = |t_n - y(x_n)|$ for all n incorrectly classified or inside margin
- Slack == 0 when the point is on or outside the margin.
- 0 > Slack < 1 for points inside the margin.
- Slack > 1 for points misclassified
