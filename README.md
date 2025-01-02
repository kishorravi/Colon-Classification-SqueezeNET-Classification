Colon Cancer Classification Using Dilated Residual SqueezeNet Variants

This repository contains the implementation of colon cancer classification using histopathological images with SqueezeNet-based architectures. The study evaluates and compares three distinct network configurations to determine their performance:
Residual SqueezeNet with Dilation
Residual SqueezeNet without Dilation
SqueezeNet with Dilation
Dataset

# Enhanced Colon Cancer Diagnosis via Dilated Residual SqueezeNet: A Deep Learning Approach



## Authors

- [@kishor_avikumar](ece.kishor@gmail.com,),[@Kishor Ravikumar](ece.kishor@gmail.com,)
- [@dr_bushara_ar](ece.kishor@gmail.com,),[@Kishor Ravikumar](ece.kishor@gmail.com,)
- [@dr_rs_vinodkumar](ece.kishor@gmail.com,),[@Kishor Ravikumar](ece.kishor@gmail.com,)
The image dataset used for this project is sourced from Kaggle: Lung and Colon Cancer Histopathological Images. This dataset was initially uploaded to Google Drive for streamlined access during experimentation.

Dataset details:
Contains 10,000 colon histopathological images.
Equally balanced between benign and adenocarcinoma tissue classes.
Each image has dimensions of 768 × 768 pixels.
The dataset was preprocessed to resize all images to 224 × 224 pixels, normalized to the [0,1] range, and split into training, validation, and test sets in a 50-25-25 ratio.
Model Architectures
Dilated Residual Colon Cancer SqueezeNet (DRCS-Net)
The DRCS-Net architecture builds on SqueezeNet by incorporating:
Dilated Convolutions: To enhance the receptive field and capture more contextual information.
Residual Connections: To mitigate gradient vanishing and improve learning of complex features.
Variants explored:
DRCS-Net.V1: Foundational residual fire module with single-scale feature extraction.
DRCS-Net.V2: Two-scale feature fusion for capturing multi-scale patterns.
DRCS-Net.V3: Three-scale feature fusion with enhanced contextual understanding using multiple dilation rates.
Results
 

Figure: Graphical Representation of Dilated Residual Squeezenet Architectures, DRCS-Net.V1, DRCS-Net.V2 and DRCS-Net.V3

Figure: Training and Validation Accuracy plots of the proposed architectures for Colon Cancer Classification (a) SqueezeNet (b) Residual SqueezeNet (c) Dilated Residual SqueezeNet (Along x-axis (horizontal): Epoch and y-axis (vertical): Accuracy)

Platform and Reproducibility
All experiments were conducted on Google Colab Pro, utilizing its GPU resources for accelerated computation. This setup ensures efficient training and validation processes.
Steps to Reproduce:
Download the dataset from the Kaggle link.
Upload the dataset to your Google Drive.
Clone this repository and open the provided Colab notebook.
Modify the dataset path in the notebook to point to your Drive location.
Train and evaluate the models as described in the scripts.
Repository Contents
residual_squeezenet_with_dilation.py: Residual SqueezeNet architecture with dilation.
residual_squeezenet_without_dilation.py: Residual SqueezeNet architecture without dilation.
squeezenet_with_dilation.py: Standard SqueezeNet architecture with dilation.
Acknowledgments
This research was conducted using the LC25000 dataset, a publicly available dataset from Kaggle.
Special thanks to the contributors of the Kaggle dataset for their invaluable work.



