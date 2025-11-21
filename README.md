# Generative Adversarial Network (GAN)

This repository contains a simple and educational implementation of a Generative Adversarial Network (GAN) using PyTorch. It demonstrates how to build a generator and discriminator, train them adversarially, and generate 28×28 grayscale images.

---

## Features

- Fully implemented Generator and Discriminator in PyTorch  
- Complete training loop for adversarial learning  
- Random noise → generated images pipeline  
- Visual outputs to monitor training progress  
- Easy-to-tweak hyperparameters (z-dim, LR, epochs, batch size, etc.)

---

## Project Structure
GAN/
├── GAN.ipynb # Main notebook with model and training code
└── README.md # Documentation (this file)



**Clone the repo:**

git clone https://github.com/karthikeyan-2023/GAN.git
cd GAN


**Launch the notebook:**

jupyter notebook GAN.ipynb


Run all cells in order to:

Build models

**Load dataset**

Train GAN

Generate sample images

How It Works
**Generator**

Takes a noise vector and transforms it into a 28×28 grayscale image.

**Discriminator**

Evaluates images (real or fake) and outputs a probability of authenticity.

****Trainin**g**

The Discriminator learns to detect real vs. fake, and the Generator learns to fool the Discriminator.
This adversarial process gradually improves the generated images.
**
Results**

After sufficient training, the Generator will begin producing digit-like images (if using MNIST).
GANs can be unstable, so results vary — but this notebook provides a clear, hands-on introduction
