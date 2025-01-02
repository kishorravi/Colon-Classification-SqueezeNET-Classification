# Enhanced Colon Cancer Diagnosis via Dilated Residual SqueezeNet: A Deep Learning Approach

## Authors

- [@kishor_avikumar](ece.kishor@gmail.com)
- [@dr_bushara_ar](bushara.ar@gmail.com)

## Contributing Authors

- [@dr_rs_vinodkumar](svinodkumar@niuniv.com)
- [@shahijulian](shahijulian@gmail.com)

## 

This repository contains the implementation of colon cancer classification using histopathological images with SqueezeNet-based architectures. The study evaluates and compares three distinct network configurations to determine their performance:
- **Residual SqueezeNet with Dilation**  
- **Residual SqueezeNet without Dilation**  
- **SqueezeNet with Dilation** 

## Dataset

The image dataset used for this project can be accessed via the following links:
- [Primary Dataset Source](https://github.com/tampapath/lung_colon_image_set)  
- [Alternate Dataset Link](https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images)

### Dataset Details:
- Contains **10,000 colon histopathological images**.
- Equally balanced between **benign** and **adenocarcinoma** tissue classes.
- Each image has dimensions of **768 × 768 pixels**.
- The dataset was preprocessed as follows:
  - Resized all images to **224 × 224 pixels**.
  - Normalized pixel values to the **[0,1] range**.
  - Split into training, validation, and test sets in a **50-25-25 ratio**.

This dataset was initially uploaded to Google Drive for streamlined access during experimentation.

## Figure 1: Samples of Histopathological Images from LC25000 Dataset

<p align="center">
  <img src="https://github.com/kishorravi/Colon-Classification-SqueezeNET-Classification/blob/main/images/colonca991.jpeg" alt="Colon Adenocarcinoma Image" width="200">
  <img src="https://github.com/kishorravi/Colon-Classification-SqueezeNET-Classification/blob/main/images/colonn947.jpeg" alt="Colon Normal Image" width="200">
</p>

<p align="center">
  <b>Figure 1:</b> Samples of Histopathological Images from LC25000 Dataset. 
  (a) Colon Adenocarcinoma Image (b) Colon Normal Image.
</p>
