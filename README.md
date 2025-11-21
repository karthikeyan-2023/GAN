GAN (karthikeyan-2023/GAN)

This repository implements a simple but instructive Generative Adversarial Network (GAN) using PyTorch for generating 28×28 grayscale image data. The goal is to provide a clear, runnable example of a GAN workflow: model definitions, training loop, and sample generation.

Features

Fully-defined Generator and Discriminator networks in PyTorch.

Training loop that alternately updates Discriminator and Generator on real and fake images.

Use of a latent noise vector (z) to generate synthetic images.

Visualization of generated samples after training (28×28 grayscale).

Easily configurable hyperparameters: latent dimension, epochs, learning rate, batch size, etc.

Project Structure
GAN/  
├── GAN.ipynb                # Jupyter Notebook with full training and sample generation  
├── (optional) models.py      # (If present) defines generator & discriminator modules  
├── (optional) utils.py       # (If present) utility functions for data loading / plotting  
└── README.md                # This file  

Requirements

Python 3.8 or higher

PyTorch (compatible version)

torchvision

matplotlib (for plotting samples)

jupyter (if you use the notebook)

Install dependencies:

pip install torch torchvision matplotlib jupyter

Usage

Clone the repository:

git clone https://github.com/karthikeyan-2023/GAN.git
cd GAN


Launch the notebook:

jupyter notebook GAN.ipynb


Execute the cells in order.
The notebook includes sections for:

defining the networks

preparing the dataset (e.g., MNIST)

training the GAN

displaying generated images at intervals

analysis of results (loss curves, sample images)

After training, inspect the “Generated Samples” section to view examples of the Generator’s output.

How It Works
Generator

Takes random noise vector z ∈ ℝ^z_dim as input and outputs a 28×28 image via a sequence of fully-connected (or maybe convolutional) layers.

Discriminator

Takes a 28×28 image (either real from the dataset or fake from the Generator) and outputs a scalar probability of being real vs. fake.

Training Loop

Load real images batch from the dataset.

Sample noise vectors and generate fake images via the Generator.

Train Discriminator to distinguish real vs. fake.

Train Generator to fool the Discriminator (i.e., maximize the probability that Discriminator labels fake as real).

Repeat for multiple epochs.

Periodically save and display generated samples and optionally track losses for both models.

Results & Expectations

With a proper number of epochs (e.g., 50–200), you should expect the Generator to gradually produce images that look more like the training data (digits, if using MNIST). The Discriminator loss tends to fluctuate as the two networks compete; mode collapse and instability are possible—this implementation is intended for educational purposes, not state-of-the-art image synthesis.
