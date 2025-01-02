## Methodology: DRCS-Net Architecture Overview

The **DRCS-Net** (Dilated Residual Colon Cancer SqueezeNet) architecture represents a significant advancement in colon cancer diagnosis, offering enhanced accuracy and efficiency in detecting cancerous tissues. This novel architecture carefully integrates cutting-edge diagnostic methods, merging key concepts of SqueezeNet with advanced features such as dilated convolutions and residual connections to improve performance.

### Key Features:
- **SqueezeNet Framework**: The base structure leverages SqueezeNet's lightweight design for efficient feature extraction.
- **Dilated Convolutions**: Adds contextual awareness by expanding the receptive field without increasing the number of parameters, enabling better detection of spatial patterns in histopathological images.
- **Residual Connections**: Facilitates effective gradient propagation, reducing the risk of vanishing gradients and ensuring smoother model training.

These components work in unison to form a robust architecture capable of early and accurate colon cancer detection.

### Workflow:
1. **Dataset Preparation**:
   - Collection of histopathology images containing both adenocarcinoma and benign samples.
   - Preprocessing steps including feature normalization and resizing of images to 224 × 224 pixels.

2. **Dataset Splitting**:
   - The dataset is divided into:
     - **Training Set**: Used for training deep learning architectures such as SqueezeNet, Residual SqueezeNet, and Dilated Residual SqueezeNet.
     - **Validation Set**: Used for model fine-tuning to prevent overfitting.
     - **Testing Set**: Used for evaluating the final performance of the trained model.

3. **Model Training**:
   - The training dataset is used to train various deep learning architectures, enabling the model to learn features through gradient-based optimization techniques.

4. **Validation**:
   - The validation dataset is employed to fine-tune the hyperparameters of the model, ensuring optimal generalization.

5. **Classification**:
   - The trained and fine-tuned model accurately distinguishes between adenocarcinoma and benign samples based on learned features from histopathological images.

### Overview of the Workflow:
<p align="center">
  <b>Fig. 1:</b> Workflow of the Overall Architecture for Colon Cancer Classification Using Histopathological Images.
</p>
<p align="center">
  <img src="https://github.com/kishorravi/Colon-Classification-SqueezeNET-Classification/blob/main/images/overall_architecture.png" alt="Overall Architecture for Colon Cancer Classification" width="400">
</p>
