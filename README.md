# 🧠 Brain Tumor Classification Using CNN

This project implements a Convolutional Neural Network (CNN) to classify brain MRI images into four categories: **glioma**, **meningioma**, **notumor**, and **pituitary**. The model is trained using TensorFlow and deployed using Gradio for a user-friendly web interface.

## 📂 Dataset

The dataset is organized with four categories of MRI images stored in respective folders:

/Training/
├── glioma/
├── meningioma/
├── notumor/
└── pituitary/

Dataset is accessed from Google Drive. Images are resized to `128x128` and normalized.

## 📦 Dependencies

Install the required libraries using pip:

```bash
pip install gradio tensorflow numpy opencv-python scikit-learn
````

## 📊 Model Architecture

* **Input:** 128x128 RGB images

* **Layers:**

  * Conv2D → MaxPooling → BatchNormalization (x3)
  * GlobalAveragePooling
  * Dense → Dropout → Output Softmax

* **Loss Function:** Categorical Crossentropy

* **Optimizer:** Adam

* **Metrics:** Accuracy

## 🚀 How to Run

1. Mount your Google Drive in Colab and set the correct `DATASET_PATH`.
2. Run all cells in `BrainTumor.ipynb`.
3. A Gradio web interface will launch where you can upload images and receive predictions.

## 💡 Features

* Classifies brain tumors into: **glioma**, **meningioma**, **notumor**, **pituitary**
* Uses a CNN trained from scratch
* Gradio-based GUI for easy interaction

## 📈 Training

* **Epochs:** 10
* **Batch Size:** 16
* **Train/Test Split:** 80/20

Performance metrics like accuracy and loss can be visualized using `history` from training.

## 🖼 Sample Inference

Upload any MRI brain scan, and the model will classify it into one of the four tumor types via an interactive interface.

## 📝 License

This project is open-source and available under the MIT License.


