# Automated Waste Classification System ♻️

An AI-powered system for **automated waste classification** that compares a lightweight CNN (**SqueezeNet**) with a modern transformer-based vision model (**MaxVit**) to evaluate trade-offs between **computational efficiency** and **classification accuracy** for real-world, sustainable deployment.

---

## Project Summary
This project classifies waste into five categories: **cardboard**, **glass**, **metal**, **paper**, and **plastic**.  
It includes training, evaluation, and a reproducible inference pipeline to demonstrate how different model families perform under resource and accuracy constraints.

---

## Dataset
- **Total images:** 2,420  
- **Classes:** Cardboard, Glass, Metal, Paper, Plastic  
- **Split:** 80% train | 10% val | 10% test  
- **Preprocessing:** Resize to model input size, normalize using ImageNet stats, and apply augmentation (random flips, rotations, zoom, brightness).

> **Note:** Place your dataset in `data/` with subfolders per class (or update paths in the scripts).

---

## Models & Key Results
- **SqueezeNet** — ~1.2M parameters — **Test accuracy: 75.10%**  
  *Lightweight — suitable for edge devices and resource-constrained deployment.*

- **MaxVit** — ~31M parameters — **Test accuracy: 95.10%**  
  *Transformer-based — higher accuracy and robustness; best for high-resource deployments.*

---

## Tech Stack
- Python  
- TensorFlow / Keras and PyTorch (experimentation)  
- NumPy, Pandas, Matplotlib  
- Image preprocessing & augmentation libraries (e.g., `torchvision` or `albumentations`)  
- Training utilities: Adam optimizers, mixed precision training

---

## Features
- End-to-end training and evaluation pipelines for both SqueezeNet and MaxVit.  
- Data augmentation and ImageNet normalization for transfer learning.  
- Reproducible experiment scripts and checkpoint saving.  
- Comparative analysis of efficiency vs. accuracy to guide deployment decisions.

---

