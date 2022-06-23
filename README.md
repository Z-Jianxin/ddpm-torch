# PyTorch Implementation of Denoising Diffusion Probabilistic Models [[paper]](https://arxiv.org/abs/2006.11239) [[official repo]](https://github.com/hojonathanho/diffusion)


## Reference formula

### Posterior mean and variance

- (Predict $x_{t-1}$ from $x_t, x_0$) 

$$ x_{t-1} \mid x_t, x_0 \sim \text{N}\left(\frac{\sqrt{\alpha_t}(1-\bar{\alpha}_{t-1})}{1-\bar{\alpha}_t}x_t+\frac{\sqrt{\alpha_{t-1}}\beta_t}{1-\bar{\alpha}_t}x_0, \sigma_t^2\right) $$

- (Predict $x_{t-1}$ from $x_t, \epsilon_t$) 


$$ x_{t-1} \mid x_t, x_0 \sim \text{N}\left(\frac{1}{\sqrt{\bar{\alpha}_t}}\left(x_t-\frac{\beta_t}{\sqrt{1-\bar{\alpha}_t}}\epsilon_t\right), \sigma_t^2\right) $$

where $\sigma_t^2 = \frac{\beta_t(1-\bar{\alpha}_{t-1})}{1-\bar{\alpha}_t}$

## Toy Example

### 8 Gaussian
![8 Gaussian](./assets/gaussian8.gif)

### 25 Gaussian
![25 Gaussian](./assets/gaussian25.gif)

### Swiss Roll
![Swiss Roll](./assets/swissroll.gif)

## Celeb-A Example

### Training samples (50 epochs)
![sample-50](./assets/celeba-sample-50.gif)

### Reverse sampling path
![reverse-process](./assets/celeba-reverse-process.gif)

