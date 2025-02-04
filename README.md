# Pinhole laser alignment for optical interferometry (DEPRECATED)

This repository is deprecated and no longer actively maintained.  For further information or assistance, please contact the repository administrator.

This project focuses on developing an advanced system for **pinhole laser alignment** in optical setups, particularly for
applications such as **interferometry** and **holography**, which demand high precision and stability. The system combines 
**machine learning** and **control theory** approaches to significantly reduce alignment times while ensuring fine-tuned 
accuracy. A **Convolutional Neural Network (CNN)** is used for **coarse adjustments** by analyzing real-time image data 
from connected cameras and making quick, general adjustments to the laser alignment in the X-Y-Z plane.

# Understanding CNN (Convolutional Neural Network) for Optical Alignments
A **Convolutional Neural Network (CNN)** is a class of deep learning models widely used for recognizing patterns in data,
such as images. In the context of this project, the CNN plays a critical role in enabling **general and fast adjustments** 
during the **pinhole laser alignment for optical interferometry**. Below is an explanation of its functionality and importance
in this application.
## Overview of CNN
A **Convolutional Neural Network** is specifically designed to process structured grid-like data, such as images, using
specialized operations called **convolutions**. In this case, it is employed to **analyze image data** and provide control
actions to adjust the laser alignment in the optical system.
### How CNN Works
The CNN processes data through layers to extract features that are relevant for making decisions. The hierarchy of layers consists of:
1. **Convolutional Layers**
These layers apply filters (kernels) to the input data to extract low-level patterns (e.g., edges, corners, etc.). As the layers go deeper, higher-level patterns (e.g., shapes, objects) are learned.
2. **Pooling Layers**
These layers reduce the dimensionality of the data, simplifying the representation and speeding up computation while retaining essential features.
3. **Fully Connected (Dense) Layers**
These layers process the extracted features and perform classification or regression tasks to make final predictions.
4. **Activation Functions** like ReLU or Sigmoid introduce non-linearity to the model, helping it learn complex patterns in the data.

In this project, CNN has been trained to interpret camera-captured images and predict X-Y axis displacement movements for fast alignment of optical components.
## Role of CNN in the Project
The CNN controller is used for **general and fast alignment** during the laser alignment process. Here's how it contributes:
1. **Image-based Predictions:**
Real-time images of the optical system are fed to the CNN, which processes them to understand the current state of alignment.
2. **Fast, Coarse Adjustment:**
Based on its analysis, the CNN provides predictions to adjust the optical components in the X-Y axes, handling large deviations quickly.

### Functional Benefits of CNN
CNN is particularly well-suited for this application because of its ability to:
- **Handle Visual Data:** Efficiently process high-dimensional data like images.
- **Quick Decision-Making:** Make rapid adjustments for reducing alignment time.
