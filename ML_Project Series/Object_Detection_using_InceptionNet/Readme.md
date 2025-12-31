# 🧠 Image Classification using InceptionV3 (CIFAR-10 & ImageNet)

This project demonstrates **transfer learning** using the **InceptionV3** deep learning architecture for image classification.  
It includes training a custom classifier on the **CIFAR-10** dataset and performing real-world image inference using a **pretrained ImageNet model**.

---

## 📌 Features

- Transfer learning with InceptionV3
- CIFAR-10 image classification
- ImageNet-based real-world prediction
- Visualization using Matplotlib and OpenCV

---

## 🗂 Project Structure

.
├── train_inception_cifar10.py  
├── predict_image.py  
├── Airplane.jpg  
├── README.md  

---

## 📦 Requirements

Install the required dependencies:

pip install tensorflow numpy matplotlib opencv-python pillow

---

## 📊 Dataset

### CIFAR-10
- 60,000 RGB images (32×32)
- 10 classes:
  airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

Loaded using `tensorflow.keras.datasets`.

---

## 🏗 Model Architecture

### Base Model
- InceptionV3 (ImageNet pretrained)
- Top layers removed
- Base layers frozen

### Custom Head
- GlobalAveragePooling2D  
- Dense (128, ReLU)  
- Dropout (0.5)  
- Dense (10, Softmax)

---

## 🔄 Data Preprocessing

- Normalize pixel values to `[0, 1]`
- Convert labels to one-hot encoding
- Resize images from `32×32` to `75×75`

---

## 🚀 Training Configuration

- Optimizer: Adam  
- Loss: Categorical Crossentropy  
- Metric: Accuracy  
- Epochs: 10  

Example:

model.fit(  
    train_images_resized,  
    train_labels,  
    epochs=10,  
    validation_data=(test_images_resized, test_labels)  
)

---

## 🧪 ImageNet Prediction

A separate pretrained InceptionV3 model is used for inference on a custom image.

### Steps
1. Load image  
2. Resize to `299×299`  
3. Apply `preprocess_input`  
4. Predict and decode ImageNet class  

Example output:

Predicted label: airplane with probability 0.92

---

## 🖼 Visualization

- Bounding box drawn for visualization
- Predicted class label displayed on image

Note: This is **classification only**, not object detection.

---

## ⚠ Notes

- CIFAR-10 and ImageNet classes are different
- ImageNet prediction uses a separate pretrained model
- Bounding box is manually added for display

---

## 🔮 Future Improvements

- Fine-tune InceptionV3 layers
- Increase training epochs
- Add data augmentation
- Export model to `.keras` or `.onnx`
- Deploy using Streamlit or FastAPI

---

## 👨‍💻 Author

Rushikesh Raghatate  
Computer Science | Deep Learning | Computer Vision
