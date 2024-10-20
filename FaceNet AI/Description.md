# **FaceNet AI: Demographic Analysis using CNN, Transfer Learning, and Data Augmentation**

## **Project Overview**

**FaceNet AI** is an advanced deep learning solution designed for **demographic analysis** from facial images. By utilizing state-of-the-art techniques such as **Convolutional Neural Networks (CNN)**, **Transfer Learning**, and **Data Augmentation**, this project aims to predict **Age**, **Gender**, and **Ethnicity** from facial data with high accuracy and efficiency. The model is built using the **UTKFace Dataset**, which consists of over 20,000 facial images, offering a wide range of demographic diversity for training and testing.

> **Want to explore the code?**  
> [Click here to view the repository.](https://github.com/SPritamDas/FaceNetAI](https://github.com/SPritamDas/Portfolio-Projects/tree/main/FaceNet%20AI/Code%20Files)

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
