# Approximating-MLE-for-multivariate-jump-diffusion-models
Implementation of paper of Kristensen, Lee, Mele: Approximate Maximum-Likelihood for Multivariate Jump-Diffusion Models with Applications to Finance.

"5.1 CIR_Vasicek.ipynb" shows the first exercise of Section 5.1 of the paper for now: approximating the transition density $p(y,u|x,t;\theta)$ of CIR model $$dx(t)=\beta(\alpha-x(t))dt+\sigma\sqrt{x(t)}dW(t)$$ via Vasicek model $$dx_{0}(t)=\beta_{0}(\alpha_{0}-x_{0}(t))dt+\sigma_{0}dW(t)$$ whose transition density is $$p_{0}(y,u|x,t;\theta_{0})=\dfrac{1}{\sqrt{\pi\gamma_{0}^{2}}}\exp{-\dfrac{(y-\alpha_{0}-(x-\alpha_{0})e^{-\beta_{0}(u-t)})^{2}}{\gamma_{0}^{2}}},$$ where $\theta_{0}=(\alpha_{0},\beta_{0},\sigma_{0}^{2}):=\theta=(\alpha,\beta,\sigma)$.

The authors fix $x=\alpha$ and $u-t=1$ and set $(\alpha,\beta,\sigma)=(0.06,0.5,0.15)$. By 4-th order terms of expansion, they obtain the approximated density as follows.

![image](https://github.com/vincentcaiwu/Approximating-MLE-for-multivariate-jump-diffusion-models/assets/132093480/9cb8cedd-86b2-459e-aadd-5ec9af30fb94)
