# geodata_ncsn
This repo is part of a project udertaken for the "Geometric Data Analysis" course taught by Jean Feydy part of the MVA (Master, Vision et Apprentissage) master

It features a simplified implementation of the paper "Generative Modeling by Estimating Gradients of the Data Distribution" Yang Song, Stefano Ermon (2019).
Its main ojective is to circumvent the manifold problem encountered during the sampling of generative models
via data noising. This idea is not new and can be linked to diffusion models. However contrarily to previous model the framework presented requires no adversarial training, no MCMC sampling during training, and no special model architecture.

The new generative model introduced is based on doing Score Matching on perturbed data at multiple levels of noise using Noise Conditional Score Network (NCSN).
Using the trained score network we can sample data from the distribution using Annealed Langevin Dynamics.

The notebook presents various content and unsuccessfully tried to exhibit a corner case for the presented method. The idea was to nestle a ring within a bigger ring hoping that starting the sampling from any point in space, the outer ring would attract more points ans thus bias the sampling from the true distribution.
Despite being unsuccessful, it showed at least the major role of the langevin noise in slow mixing between the different components of the distribution. 

Here is the [report](Report.pdf) of our class project cowritten with Hanna Benarroch and Virgile Richard


Key resources:
  - Link to the paper : https://arxiv.org/abs/1907.05600
  - Paper's repo : https://github.com/ermongroup/ncsn
  - Very informative author's post : https://yang-song.net/blog/2021/score/
  - Very interesting blog on diffusion models in general https://lilianweng.github.io/posts/2021-07-11-diffusion-models/
