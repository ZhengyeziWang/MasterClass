# MasterClass
# 🎨 Deep Image Harmonization with U-Net and Perceptual Loss

This repository contains the implementation of a deep learning–based image harmonization pipeline using a U-Net architecture, global-local feature fusion, and perceptual loss. The project was developed as part of a course-based research assignment, focusing on solving color inconsistencies between foreground and background in composite images.

---

## 📌 Project Highlights

- ✅ Built from scratch using PyTorch and Jupyter Notebook
- ✅ Uses [ccHarmony](https://github.com/bcmi/ImageHarmonizationDataset-ccHarmony) dataset for real-world lighting variations
- ✅ U-Net backbone with perceptual loss (VGG16) and attention mechanism (GIFT)
- ✅ Mask-guided output fusion to preserve background consistency
- ✅ Includes batch-size tuning, training-stage comparison, and qualitative evaluation

---

## 🖼️ Model Architecture

<div align="center">
  <img src="mastercalss-.drawio.png" alt="Model Structure" width="800"/>
</div>

The model is based on U-Net with a two-level encoder-decoder, followed by global average pooling and a GIFT module to enhance channel-wise attention. A foreground mask is used at inference time to ensure that only the foreground is altered.

---

## 📁 Dataset

We use the **ccHarmony** dataset, which offers realistic foreground-background mismatch conditions through lighting variation.

- 🔗 Dataset link: [ccHarmony (Google Drive)](https://drive.google.com/drive/folders/1ADh3RAN5EKQmeuCtDKtzkl-kJIB4JbAU?usp=drive_link)
- 📦 Subset used for quick validation (dataset_clean_1000)
- 🧪 Full dataset used for final training (initial_dataset)

---

### 📸 Test Images (Separate from Dataset)

To evaluate the trained model on novel or unseen composite images, you can use the sample test set provided below:

- 📁 Test images (Google Drive): [Download Link](https://drive.google.com/drive/folders/1S3UmYg7Dx2bIB9s5P4-QoXFIhHeu2306?usp=sharing)

These images are not part of the ccHarmony dataset and are used for visual evaluation only. They follow the same format: composite image + GroundTruth.

---

## 📦 Pretrained Weights

- 📥 [Download trained model weights (Google Drive)](https://drive.google.com/drive/folders/1NfVQSRNqO-n3ktuQz3pYxS9Bh6TEWzW3?usp=drive_link)
- File format: `.pth`  
- Saved weights trained for 30, 50, and 70 epochs, with decreasing batch size and using perceptual supervision

---

## 📓 Jupyter Notebook

The core implementation is in:

```bash
📘 MasterClass_final.ipynb

---

##  📚 Citation


@inproceedings{niu2023,
title={ccHarmony: Color-Checker Guided Illumination Estimation for Image Harmonization},
author={Niu, Yuge and Zhou, Hong and Huang, Xinxin and Deng, Cheng and Ding, Xuan and Yao, Wei and Dong, Xiaopeng},
booktitle={Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)},
year={2023},
pages={6481--6491}
}

🔗 Dataset GitHub: [https://github.com/bcmi/Image-Harmonization-Dataset-ccHarmony](https://github.com/bcmi/Image-Harmonization-Dataset-ccHarmony)


