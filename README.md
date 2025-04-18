# 🌿 Plant Disease Classification using CNN

## 📌 Project Title:

**Plant Disease Classification using Convolutional Neural Networks (CNN)**

## 🎯 Purpose / Aim:

To develop a deep learning-based image classification system that accurately identifies different types of plant diseases from leaf images. The model helps in early detection of diseases, assisting farmers and agricultural experts in taking timely actions.

## 🎯 Objectives:

- Utilize the PlantVillage dataset with segmented plant leaf images.
- Build and train a CNN model to classify plant diseases.
- Achieve high accuracy with image preprocessing and augmentation.
- Visualize training and testing results for better understanding.

## 🛠️ Technologies & Libraries Used:

- Python
- Google Colab
- TensorFlow / Keras
- Matplotlib
- NumPy
- Pillow (PIL)
- Kaggle API

## 📊 Dataset Used:

- **Name:** PlantVillage Dataset
- **Source:** [Kaggle - PlantVillage Dataset](https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset)
- **Type:** Segmented leaf images
- **Classes:** Multiple plant disease categories (e.g., Apple Scab, Grape Black Rot, Healthy, etc.)

## 🧠 CNN Model Architecture:

```plaintext
1. Conv2D (32 filters, 3x3, ReLU)
2. MaxPooling2D (2x2)
3. Conv2D (64 filters, 3x3, ReLU)
4. MaxPooling2D (2x2)
5. Conv2D (128 filters, 3x3, ReLU)
6. MaxPooling2D (2x2)
7. Flatten
8. Dense (128 units, ReLU)
9. Output Dense (15 units, Softmax)
```

## ⚙️ Model Training:

- **Loss Function:** Categorical Crossentropy
- **Optimizer:** Adam
- **Batch Size:** 32
- **Epochs:** 15
- **Image Augmentation:** Yes (rotation, shear, zoom, flip)

## 📈 Performance:

- **Training Accuracy:** ~99%
- **Validation Accuracy:** ~97%

## 🗓️ Model Summary:

```
Layer (type)                 Output Shape              Param #
=================================================================
Conv2D                      (None, 64, 64, 32)         896
MaxPooling2D                (None, 32, 32, 32)         0
Conv2D                      (None, 30, 30, 64)         18496
MaxPooling2D                (None, 15, 15, 64)         0
Conv2D                      (None, 13, 13, 128)        73856
MaxPooling2D                (None, 6, 6, 128)          0
Flatten                     (None, 4608)               0
Dense                       (None, 128)                589952
Dense                       (None, 15)                 1935
=================================================================
Total Parameters: 685,135
Trainable Parameters: 685,135
```

## 🔧 Setup Instructions:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```
2. Install required libraries:
   ```bash
   pip install tensorflow matplotlib numpy pillow kaggle
   ```
3. Add your `kaggle.json` file for API access:
   - Upload it in the same directory.
   - Load and configure using:
     ```python
     import json, os
     kaggle_credentails = json.load(open("kaggle.json"))
     os.environ['KAGGLE_USERNAME'] = kaggle_credentails["username"]
     os.environ['KAGGLE_KEY'] = kaggle_credentails["key"]
     ```
4. Run the notebook in Google Colab or Jupyter.

## 📌 Key Takeaways:

- CNN performs exceptionally well for image classification in agriculture.
- The use of segmented images boosts accuracy by removing background noise.
- With proper preprocessing and augmentation, model overfitting is minimized.
- This project can be extended into real-time mobile applications for farmers.

## 👥 Contributors:

| Contributor | GitHub Profile |
|-------------|----------------|
| Niyar Rane | [@Niyar07](https://github.com/Niyar07) |
| Lobhesh Sambare | [@lobsam1222](https://github.com/lobsam1222) |
| Pawan Thakre | [@pawan185](https://github.com/pawan185) |

---
