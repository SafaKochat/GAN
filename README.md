# 🔥 Thermal Image Analysis & GAN Generation

This project performs **Exploratory Data Analysis (EDA)** and trains a **Generative Adversarial Network (GAN)** on a dataset of thermal images of an induction motor. The goal is to analyze the dataset distribution and generate synthetic thermal images using deep learning.

---

## 🚀 Project Objectives

- Perform Exploratory Data Analysis (EDA) on thermal image dataset
- Visualize class distribution and dataset characteristics
- Preprocess and augment thermal images
- Build a custom GAN (Generator + Discriminator)
- Train the GAN to generate synthetic thermal images
- Compare generated images with real images using correlation analysis

---

## 🧠 Key Features

- 📊 Dataset analysis (class distribution, pixel intensity, image sizes)
- 🖼️ Visualization of sample images per class
- ⚙️ Image preprocessing (resize, normalization)
- 🔄 Data augmentation using Keras ImageDataGenerator
- 🧬 Custom GAN implementation in TensorFlow
- 🎨 Image generation after each training epoch
- 📈 Correlation analysis between real and generated images

---

## 🛠️ Technologies Used

- Python 3
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- PIL (Pillow)
- Kaggle Notebook Environment

---

## 📁 Dataset

The dataset is loaded from Kaggle: /kaggle/input/thermal-images-of-induction-motor

It contains multiple classes of thermal images representing different conditions of an induction motor.

---

## ⚙️ Project Pipeline

### 1. Exploratory Data Analysis (EDA)
- Count number of images per class
- Visualize class distribution
- Display sample images
- Analyze image dimensions
- Analyze pixel intensity distribution

---

### 2. Data Preprocessing
- Resize images to 64×64
- Normalize pixel values to [-1, 1]
- Convert images to RGB format

---

### 3. Data Augmentation
Applied transformations:
- Rotation
- Shift (width & height)
- Zoom
- Shear
- Horizontal flip

Each image is augmented multiple times to increase dataset diversity.

---

### 4. GAN Architecture

#### Generator
- Dense layer → Reshape → Conv2DTranspose layers
- Outputs 64×64×3 images
- Uses Batch Normalization + ReLU
- Final activation: **tanh**

#### Discriminator
- Convolutional layers with LeakyReLU
- Dropout for regularization
- Outputs real/fake classification score

---

## 🧪 Training

- Optimizer: Adam (learning rate = 1e-4)
- Loss: Binary Crossentropy
- Epochs: 200
- Batch size: 32

During training:
- Generator creates synthetic images
- Discriminator learns to distinguish real vs fake
- Loss values are tracked for both models

---

## 📊 Results

- Generated images are visualized after each epoch
- Final evaluation includes:
  - Visual comparison (real vs generated images)
  - Pixel-level correlation analysis

Example output:
<img width="490" height="487" alt="Capture d&#39;écran 2026-06-28 154204" src="https://github.com/user-attachments/assets/2ad5640e-dca3-46ed-938e-c3d1cb5d8905" />
<img width="488" height="478" alt="Capture d&#39;écran 2026-06-28 154145" src="https://github.com/user-attachments/assets/06797a6a-71f6-498b-a657-596b4c063563" />

---

## 📷 Sample Outputs

- Class distribution bar chart
- Sample images per class
- Pixel intensity histogram
- Generated images from GAN
- Side-by-side comparison of real vs synthetic images

---

## 📌 Future Improvements

- Improve GAN stability (DCGAN / WGAN-GP)
- Add FID score for better evaluation
- Train on higher resolution images
- Add conditional GAN (cGAN) for class-based generation
- Deploy model as a web app (Streamlit / Flask)

---

## ⚠️ Notes

- This project is designed for Kaggle environments
- Large augmentation increases training time significantly
- GAN training may be unstable without tuning

---

## 👩‍💻 Author

Developed by Safa Kochat  
AI & Deep Learning Enthusiast 🤖🔥

