Semantic Segmentation of the Left Ventricle from 2D Cardiac MRI Images using U-Net
This repository contains a Jupyter notebook implementing U-Net for semantic segmentation of the left ventricle from 2D cardiac MRI images. Here’s a breakdown of the main sections in the notebook:

1. Importing Libraries
The notebook begins by importing essential libraries such as TensorFlow, NumPy, Matplotlib, OpenCV, and scikit-learn. These are required for building the model, data processing, and visualization.

2. Data Preprocessing
This section handles data loading, resizing, normalization, and augmentation to improve model performance. It typically involves reading MRI slices and their corresponding segmentation masks, resizing them to a fixed size (e.g., 256x256), and scaling pixel values.

3. Building the U-Net Model

The core of this notebook is the U-Net model definition. It includes an encoder-decoder structure with skip connections:
Encoder: Extracts features using convolution and max-pooling.
Decoder: Upsamples the extracted features to match the original image dimensions.
Skip Connections: Helps preserve spatial information by combining features from encoder and decoder stages.

4. Model Training
The model is compiled with a loss function (typically binary cross-entropy for single-class segmentation) and an optimizer (like Adam). It then trains using the preprocessed MRI slices and masks.

5. Model Evaluation
After training, the model’s performance is evaluated using validation data, providing metrics like accuracy and loss.

6. Predictions and Visualization
Finally, the notebook generates segmentation masks for test images and visualizes the results alongside ground truth masks for qualitative analysis.
