# Radon-Transform-Denoising
Comparing classical regularisation approaches to deep learning for the task of denoising data generated from the radon transform process.

The data examined is the [Shepp–Logan phantom](https://en.wikipedia.org/wiki/Shepp%E2%80%93Logan_phantom).

![Shepp–Logan phantom](assets/phantom.png)

When the radon transform (and inverse) are applied using adequately sampled points with no noise, a near perfect reconstruction can occur.

![Reconstructed Shepp–Logan phantom](assets/residualsIdeal.png)

However, noise in the forward transform leads to a distinctive radial noise pattern in resulting reconstruction, due to the integration step of the analytical solution.

![Noisy Shepp–Logan phantom](assets/noisy.png)

## Classic regularisation denoising
Classic regularisation techniques are show, specifically zero-order and first-order tikhonov regularisation, which mitigate some of the effects but radial noise remains.

![Regularisation Shepp–Logan phantom](assets/classicalMethods.png)

## Deep Learning denoising
A deep learning model with a UNet design is trained on synthesised data with varying levels of noise applied.

![Deep Learning validation](assets/validationData.png)

Performance is then evaluated on the original Shepp–Logan phantom at varying noise levels.

![Deep Learning test Shepp–Logan phantom](assets/phantomReconstruction.png)
