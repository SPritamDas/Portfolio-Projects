# **FaceNet AI: Demographic Analysis using CNN, Transfer Learning, and Data Augmentation**

## **Project Overview**

**FaceNet AI** is an advanced deep learning solution designed for **demographic analysis** from facial images. By utilizing state-of-the-art techniques such as **Convolutional Neural Networks (CNN)**, **Transfer Learning**, and **Data Augmentation**, this project aims to predict **Age**, **Gender**, and **Ethnicity** from facial data with high accuracy and efficiency. The model is built using the **UTKFace Dataset**, which consists of over 20,000 facial images, offering a wide range of demographic diversity for training and testing.

> **Want to explore the code?**  
> [Click here to view the repository.](https://github.com/SPritamDas/Portfolio-Projects/tree/main/FaceNet%20AI/Code%20Files)

## **Key Features**
- **Age Estimation**: Predict a person’s age using facial characteristics.
- **Gender Classification**: Classify gender (male or female) based on facial features.
- **Ethnicity Recognition**: Identify the ethnicity (White, Black, Asian, etc.) from facial images.
- **Transfer Learning**: Leverage pre-trained models (VGG16) for faster training and enhanced accuracy.
- **Data Augmentation**: Apply image transformations (rotation, scaling, flipping) to enrich the dataset and reduce overfitting.

## **Dataset Information**

The **UTKFace Dataset** is a large-scale dataset comprising over 20,000 facial images. These images span a wide age range (0–116 years) and include annotations for **age**, **gender**, and **ethnicity**. The dataset captures a broad variety of poses, expressions, illumination, and occlusions, making it ideal for training robust facial recognition models.

- **Dataset Download**: [UTKFace Dataset](https://susanqq.github.io/UTKFace/)

## **Technical Details**

The model architecture combines **CNN** with **Transfer Learning** using the **VGG16** model, fine-tuned on the UTKFace dataset to predict age, gender, and ethnicity.

### **Architecture Highlights**:
- **Base Model**: VGG16, pre-trained on ImageNet, to extract relevant features from facial images.
- **Fine-Tuning**: The top layers of VGG16 are retrained on the UTKFace dataset to adapt the model for the specific task of demographic analysis.
- **Data Augmentation**: Techniques like random rotations, flips, and zooms are applied to the training dataset, improving model generalization.
- **Optimizer**: Adam optimizer for efficient training.
- **Loss Function**: Categorical Cross-Entropy for multi-class classification tasks.

### Model Architecture

| Layer Type            | Output Shape           | Param #       | Connected to               |
|-----------------------|------------------------|---------------|----------------------------|
| **Input Layer**        | (None, 224, 224, 3)     | 0             | -                          |
| **Block 1**            |                        |               |                            |
| Conv2D (block1_conv1)  | (None, 224, 224, 64)    | 1,792         | input_layer[0][0]          |
| Conv2D (block1_conv2)  | (None, 224, 224, 64)    | 36,928        | block1_conv1[0][0]         |
| MaxPooling2D (block1_pool) | (None, 112, 112, 64) | 0             | block1_conv2[0][0]         |
| **Block 2**            |                        |               |                            |
| Conv2D (block2_conv1)  | (None, 112, 112, 128)   | 73,856        | block1_pool[0][0]          |
| Conv2D (block2_conv2)  | (None, 112, 112, 128)   | 147,584       | block2_conv1[0][0]         |
| MaxPooling2D (block2_pool) | (None, 56, 56, 128)  | 0             | block2_conv2[0][0]         |
| **Block 3**            |                        |               |                            |
| Conv2D (block3_conv1)  | (None, 56, 56, 256)     | 295,168       | block2_pool[0][0]          |
| Conv2D (block3_conv2)  | (None, 56, 56, 256)     | 590,080       | block3_conv1[0][0]         |
| Conv2D (block3_conv3)  | (None, 56, 56, 256)     | 590,080       | block3_conv2[0][0]         |
| MaxPooling2D (block3_pool) | (None, 28, 28, 256)  | 0             | block3_conv3[0][0]         |
| **Block 4**            |                        |               |                            |
| Conv2D (block4_conv1)  | (None, 28, 28, 512)     | 1,180,160     | block3_pool[0][0]          |
| Conv2D (block4_conv2)  | (None, 28, 28, 512)     | 2,359,808     | block4_conv1[0][0]         |
| Conv2D (block4_conv3)  | (None, 28, 28, 512)     | 2,359,808     | block4_conv2[0][0]         |
| MaxPooling2D (block4_pool) | (None, 14, 14, 512)  | 0             | block4_conv3[0][0]         |
| **Block 5**            |                        |               |                            |
| Conv2D (block5_conv1)  | (None, 14, 14, 512)     | 2,359,808     | block4_pool[0][0]          |
| Conv2D (block5_conv2)  | (None, 14, 14, 512)     | 2,359,808     | block5_conv1[0][0]         |
| Conv2D (block5_conv3)  | (None, 14, 14, 512)     | 2,359,808     | block5_conv2[0][0]         |
| MaxPooling2D (block5_pool) | (None, 7, 7, 512)    | 0             | block5_conv3[0][0]         |
| **Flatten**            | (None, 25088)          | 0             | block5_pool[0][0]          |
| **Dense Layers**       |                        |               |                            |
| Dense (dense)          | (None, 512)            | 12,845,568    | flatten[0][0]              |
| Dense (dense_4)        | (None, 512)            | 12,845,568    | flatten[0][0]              |
| Dense (dense_8)        | (None, 512)            | 12,845,568    | flatten[0][0]              |
| Dense (dense_1)        | (None, 256)            | 131,328       | dense[0][0]                |
| Dense (dense_5)        | (None, 256)            | 131,328       | dense_4[0][0]              |
| Dense (dense_9)        | (None, 256)            | 131,328       | dense_8[0][0]              |
| Dense (dense_2)        | (None, 128)            | 32,896        | dense_1[0][0]              |
| Dense (dense_6)        | (None, 128)            | 32,896        | dense_5[0][0]              |
| Dense (dense_10)       | (None, 128)            | 32,896        | dense_9[0][0]              |
| Dense (dense_3)        | (None, 64)             | 8,256         | dense_2[0][0]              |
| Dense (dense_7)        | (None, 64)             | 8,256         | dense_6[0][0]              |
| Dense (dense_11)       | (None, 64)             | 8,256         | dense_10[0][0]             |
| **Output Layers**      |                        |               |                            |
| Dense (age)            | (None, 1)             | 65            | dense_3[0][0]              |
| Dense (gender)         | (None, 1)             | 65            | dense_7[0][0]              |
| Dense (ethnicity)      | (None, 5)             | 325           | dense_11[0][0]             |
| **Total params**       |                        | **53,769,287**|                            |
| **Trainable params**   |                        | **39,054,599**|                            |
| **Non-trainable params**|                       | **14,714,688**|                            |
