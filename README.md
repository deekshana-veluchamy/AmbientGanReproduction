# AmbientGanReproduction

As part of the International Conference on Learning Representations reproducibility challenge we attempted to reproduce some of the experiments in [AmbientGAN: Generative models from lossy measurements](https://openreview.net/pdf?id=Hy7fDog0b) ; a twist on the traditional baseline generative adversarial network where it is assumed that the underlying state vector is not directly observed-- instead the model must learn from images with various noise transformations applied.

In this repo we reproduce the work in the Ambient paper for block pixel transformations using the MNIST. To do so, we follow the paper in creating two baseline GAN models -- one that ignores that any transformation has taken place, and another that makes use of inverse transformations which we compare with the Ambient network using inception scoring. Below is a schematic of the three architectures. We direct the interested reader to [ICLR Reproducibility Challenge, Ambient GAN](https://github.com/COMP6248-Reproducability-Challenge/AmbientGanReproduction/blob/master/Reproduction_Paper.pdf) for full details of our experiements.


![alt text](https://github.com/COMP6248-Reproducability-Challenge/AmbientGanReproduction/blob/master/model_flow.png "Logo Title Text 1")


# Code Files 

### code/BASELINE_GAN.ipynb 

Contains the code for Baseline GAN Experiments

### code/IgnoreGan.ipynb

Contains the code for ignore model Experiments 

### code/AmbientGan.ipynb

Contains the code for Ambient model Experiments 

# Results 

Our reproduced results confirm that the ambient approach training on noisy-images indeed gives improvement over GAN methods that do not account for the noise as well as baseline GANs trained after de-noising approaches.

![Click me to see the graphed results](https://github.com/COMP6248-Reproducability-Challenge/AmbientGanReproduction/blob/master/model_comparison.pdf "Click me to see the graphed results ")

# Examples 

Below is an example set of generated MNIST digits with a block-pixel transformation p = 0.9 trained with Ambient (left), Baseline with Bi-harmonic in-painting (center) and Ignore (right)

<p align="center">
  <img width="600" height="200" src="https://github.com/COMP6248-Reproducability-Challenge/AmbientGanReproduction/blob/master/examples.PNG">
</p>





