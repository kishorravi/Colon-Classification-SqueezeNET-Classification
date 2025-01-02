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
  - Split into training, validation, and test sets with the following ratios:
    - **Training Set:** 50% of the dataset.
    - **Validation Set:** 25% of the dataset.
    - **Test Set:** 25% of the dataset.

<p align="center">
  <img src="https://github.com/kishorravi/Colon-Classification-SqueezeNET-Classification/blob/main/images/colonca991.jpeg" alt="Colon Adenocarcinoma Image" width="200">
  <img src="https://github.com/kishorravi/Colon-Classification-SqueezeNET-Classification/blob/main/images/colonn947.jpeg" alt="Colon Normal Image" width="200">
</p>

<p align="center">
  <b>Figure 1:</b> Samples of Histopathological Images from LC25000 Dataset. 
  (a) Colon Adenocarcinoma Image (b) Colon Normal Image.
</p>

This dataset was initially uploaded to Google Drive for streamlined access during experimentation.

## Methodology: DRCS-Net Architecture Overview

The **DRCS-Net** (Dilated Residual Colon Cancer SqueezeNet) architecture represents a significant advancement in colon cancer diagnosis, offering enhanced accuracy and efficiency in detecting cancerous tissues. This novel architecture carefully integrates cutting-edge diagnostic methods, merging key concepts of SqueezeNet with advanced features such as dilated convolutions and residual connections to improve performance.

### Key Features:
- **SqueezeNet Framework**: The base structure leverages SqueezeNet's lightweight design for efficient feature extraction.
- **Dilated Convolutions**: Adds contextual awareness by expanding the receptive field without increasing the number of parameters, enabling better detection of spatial patterns in histopathological images.
- **Residual Connections**: Facilitates effective gradient propagation, reducing the risk of vanishing gradients and ensuring smoother model training.

### Workflow:
1. **Dataset Preparation**:
   - Collection of histopathology images containing both adenocarcinoma and benign samples.
   - Preprocessing steps including feature normalization and resizing of images to 224 × 224 pixels.

2. **Dataset Splitting**:
   - The dataset is divided into:
     - **Training Set:** Used for training deep learning architectures such as SqueezeNet, Residual SqueezeNet, and Dilated Residual SqueezeNet.
     - **Validation Set:** Used for model fine-tuning to prevent overfitting.
     - **Testing Set:** Used for evaluating the final performance of the trained model.

3. **Model Training**:
   - The training dataset is used to train various deep learning architectures, enabling the model to learn features through gradient-based optimization techniques.

4. **Validation**:
   - The validation dataset is employed to fine-tune the hyperparameters of the model, ensuring optimal generalization.

5. **Classification**:
   - The trained and fine-tuned model accurately distinguishes between adenocarcinoma and benign samples based on learned features from histopathological images.

### Overview of the Workflow:

<p align="center">
  <img src="https://github.com/kishorravi/Colon-Classification-SqueezeNET-Classification/blob/main/images/BLOCK%20DIAGRAM%20(6).jpg" width="800">
</p>
<p align="center">
  <b>Fig. 2:</b> Workflow of the Overall Architecture for Colon Cancer Classification Using Histopathological Images.
</p>

## Results and Discussion

The experimental evaluation highlights the superior performance of the proposed DRCS-Net architecture for colon cancer classification. The results for the three variants of DRCS-Net (V1, V2, V3), along with comparisons to SqueezeNet and Residual SqueezeNet, are presented below.

### Model Performance Metrics
<p align="center">
  <img src="https://github.com/kishorravi/Colon-Classification-SqueezeNET-Classification/blob/main/images/table.jpeg" width="800">
</p>
<p align="center">
  <b>Fig. 2:</b>  Performance Comparison of Dilated Residual SqueezeNet Architectures,DRCS-Net.V1, DRCS-Net.V2, and DRCS-Net.V3
</p>


### Key Insights
1. **Accuracy**:
   - The proposed DRCS-Net.V3 achieves the highest accuracy of 99.80%, outperforming both SqueezeNet and Residual SqueezeNet.
2. **Precision and Recall**:
   - DRCS-Net.V3 exhibits exceptional precision (99.90%) and recall (99.60%), indicating its ability to accurately identify and differentiate between adenocarcinoma and benign tissues.
3. **F1-Score**:
   - A balanced F1-Score of 99.74% further confirms the robustness of DRCS-Net.V3 in colon cancer classification.

### Confusion Matrix Summary
The confusion matrix for DRCS-Net.V3 reveals minimal misclassifications:
- Only 1 adenocarcinoma sample was misclassified as benign.
- Only 4 benign samples were misclassified as adenocarcinoma.

### Graphical Representation
The graphical representation of accuracy, precision, recall, and specificity for the proposed architectures is illustrated below:

<p align="https://github.com/kishorravi/Colon-Classification-SqueezeNET-Classification/blob/main/images/table.jpeg" width="800">
</p>
<p align="center">
  <b>Fig. 2:</b>  Performance Comparison of Dilated Residual SqueezeNet Architectures,DRCS-Net.V1, DRCS-Net.V2, and DRCS-Net.V3
</p>


### Comparison with State-of-the-Art
The proposed DRCS-Net also surpasses existing state-of-the-art methods, achieving the highest performance metrics across all evaluation criteria:

| Author          | Model            | Accuracy (%) | Precision (%) | Recall (%) | F1-Score (%) |
|------------------|------------------|--------------|---------------|------------|--------------|
| Javed [40]       | CNN              | 89.80        | 93.60         | 89.80      | 91.40        |
| Kumar [41]       | DenseNet-121     | 98.60        | 98.63         | 98.60      | 98.50        |
| Younas [42]      | GoogLeNet        | 86.70        | 86.60         | 86.60      | 87.10        |
| Chlorogiannis [43]| CNN             | 99.69        | 99.31         | -          | 99.00        |
| **Proposed**     | **DRCS-Net.V3**  | **99.80**    | **99.90**     | **99.60**  | **99.74**    |

These results confirm the potential of DRCS-Net as a transformative tool for early and accurate colon cancer diagnosis using histopathological images.
