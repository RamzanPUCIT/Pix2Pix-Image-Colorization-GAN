# Pix2Pix-Image-Colorization-GAN

A Pix2Pix Conditional GAN project for automatic image colorization using the CIFAR-10 dataset implemented in PyTorch.

---

# Project Overview

This project focuses on grayscale-to-color image translation using a Conditional Generative Adversarial Network (cGAN) inspired by the Pix2Pix architecture.

The model learns how to generate realistic RGB images from grayscale inputs using adversarial learning.

The project was implemented as part of Generative Modeling coursework during M.Phil Artificial Intelligence studies at PUCIT, University of the Punjab, Lahore.

---

# Objectives

- Convert grayscale images into realistic color images
- Understand Conditional GAN and Pix2Pix architecture
- Learn image-to-image translation using deep learning
- Evaluate generated images using image quality metrics

---

# Dataset

## CIFAR-10 Dataset

The project uses the CIFAR-10 dataset containing:

- 60,000 images
- 10 object classes
- Image size: 32×32 RGB

### Classes:
- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

---

# Model Architecture

## Generator
- Encoder-Decoder style CNN
- Converts grayscale image (1 channel) into RGB image (3 channels)

## Discriminator
- PatchGAN Discriminator
- Distinguishes between:
  - Real color images
  - Generated color images

---

# Technologies Used

- Python
- PyTorch
- Google Colab
- NumPy
- Matplotlib
- PIL
- scikit-image

---

# Features

- Conditional GAN (Pix2Pix-style)
- Generator + PatchGAN Discriminator
- Grayscale → RGB translation
- Best model checkpoint saving
- Resume training support
- Epoch-wise generated image saving
- Loss curve visualization
- PSNR metric
- SSIM metric
- Custom image testing

---

# Training Details

| Parameter | Value |
|---|---|
| Epochs | 20 |
| Batch Size | 64 |
| Optimizer | Adam |
| Learning Rate | 0.0002 |
| Loss Functions | BCE + L1 Loss |
| Framework | PyTorch |
| Device | CUDA GPU |

---

# Evaluation Metrics

## PSNR Score
Measures image reconstruction quality.

```text
Average PSNR ≈ 10.71
```

## SSIM Score
Measures structural similarity between generated and real images.

```text
Average SSIM ≈ 0.63
```

---

# Results

The model successfully learned approximate colorization from grayscale images.

Generated images preserve:
- object structure
- semantic regions
- approximate color tones

Due to CIFAR-10 low resolution (32×32), outputs appear slightly blurry.

---

# Sample Workflow

```text
Grayscale Image
       ↓
Generator
       ↓
Generated Color Image
       ↓
PatchGAN Discriminator
       ↓
Real / Fake Decision
```

---

# Repository Structure

```text
Pix2Pix-Image-Colorization-GAN/
│
├── Results/
├── checkpoints/
├── generated_images/
├── plots/
├── README.md
├── LICENSE
└── notebook.ipynb
```

---

# Future Improvements

- Higher resolution datasets
- Full U-Net Pix2Pix architecture
- Attention-based GANs
- FID score evaluation
- Streamlit web app deployment
- CelebA / Landscape datasets

---

# Learning Outcomes

This project helped in understanding:

- Conditional GANs
- Image-to-Image Translation
- Deep Learning pipelines
- Adversarial Training
- Model evaluation metrics
- Research-oriented experimentation

---

# Author

## Muhammad Ramzan
M.Phil Artificial Intelligence  
Punjab University College of Information Technology (PUCIT)  
University of the Punjab, Lahore  

GitHub: https://github.com/RamzanPUCIT

---

# License

This project is licensed under the MIT License.

---

# Acknowledgment

Special thanks to respected teachers and classmates for guidance and discussions during the Generative Modeling course.
