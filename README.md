# GAN (Generative Adversarial Network)

This repository contains an introductory Generative Adversarial Network (GAN) implementation using PyTorch. The project demonstrates how to build a Generator and Discriminator, train them on 28×28 grayscale images, and generate synthetic samples.

---

## 📁 Project Files

- **GAN.ipynb** — Main notebook with model definitions, training loop, and sample generation  
- **README.md** — Documentation

---

## 🔧 Requirements

Install the necessary packages:

```bash
pip install torch torchvision matplotlib jupyter
🚀 How to Run
Clone the repository:

bash
Copy code
git clone https://github.com/karthikeyan-2023/GAN.git
cd GAN
Open the notebook:

bash
Copy code
jupyter notebook GAN.ipynb
Run the cells in sequence to train the GAN and view generated images.

🧠 How the GAN Works
Generator
Takes random noise as input

Produces a 28×28 grayscale image

Discriminator
Receives an image (real or generated)

Outputs a probability indicating whether the image is real

Training
Both networks train against each other

The Generator tries to fool the Discriminator

The Discriminator tries to detect fakes

📈 Output
After training, the notebook generates images created by the GAN based on random noise input.

💡 Possible Enhancements
Switch to a DCGAN architecture

Add checkpoints and sample saving

Add metrics like FID or Inception Score

Try different image datasets

