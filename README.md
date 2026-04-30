# SliceMAE: Efficient Brain Tumor Segmentation from MRI Using a 2D Slice-Based MAE-UNet

This project presents a deep learning-based system for automated brain tumor segmentation from multimodal MRI scans. Developed as a final-year capstone thesis, the work focuses on improving segmentation accuracy while reducing dependency on large labeled datasets through the use of self-supervised learning.

## Overview

Brain tumor segmentation plays a critical role in medical diagnosis and treatment planning. Manual annotation is time-consuming and subject to variability. This project addresses these challenges by combining self-supervised learning with convolutional neural networks to build a data-efficient and scalable segmentation system.

## Methodology

The system follows a two-stage learning approach:

* Self-supervised pretraining using Masked Autoencoder (MAE) and Dense Contrastive Learning (DenseCL)
* Supervised fine-tuning using segmentation architectures

Multiple models are implemented and evaluated:

* U-Net
* Vision Transformer (ViT)
* UNETR
* TransUNet

The final proposed model, MAE-UNet, integrates MAE-based pretraining with a U-Net decoder for improved segmentation performance.

## Dataset

The project utilizes the BraTS 2020 dataset, which includes multimodal MRI scans (T1, T1ce, T2, FLAIR) along with expert-annotated segmentation masks.

## Implementation

The system is implemented in Python using deep learning frameworks and FAISS-independent pipelines for model training and evaluation. A slice-based 2D processing strategy is used to reduce computational complexity while maintaining strong performance.

## Results

The experimental results demonstrate that self-supervised learning significantly improves segmentation performance:

* U-Net (supervised baseline): Dice Score ~83.9%
* MAE-UNet (proposed model): Dice Score ~74.55%

The model shows improved performance across challenging tumor regions and better generalization.

## Project Structure

notebooks/ – Supervised and self-supervised model implementations
live_demo/ – Web deployment and live demo access

## How to Run

Install dependencies:
pip install -r requirements.txt

Run the notebooks located in the notebooks/ directory for training and evaluation.

## Project Status

This project is developed as a capstone thesis and is currently being extended for Scopus(IJCDS) Q2 Journal, with ongoing improvements in model performance, evaluation, and system integration.

## Conclusion

This work demonstrates that integrating self-supervised learning with CNN-based architectures can significantly enhance brain tumor segmentation performance while reducing reliance on labeled data. The proposed approach provides a practical and scalable solution for medical image analysis.


