
# 🌾 Wheat Head Detection using Faster R-CNN (ResNet50)

This project demonstrates **object detection** using the **Faster R-CNN** deep learning architecture with a **ResNet50 backbone**.  
It focuses on detecting **wheat heads in agricultural field images** using the **Global Wheat Detection dataset** and **PyTorch**.

---

## 📌 Features

- Object detection with Faster R-CNN  
- Bounding box regression for wheat heads  
- Custom dataset handling  
- Visualization of predictions using Matplotlib  
- PyTorch-based training pipeline  

---

## 🗂 Project Structure


├── wheat_detection_faster_rcnn_resnet50.ipynb  
├── README.md  
├── results/  
│   ├── result_1.png  
│   ├── result_2.png  
│   ├── result_3.png  
│   └── result_4.png  

---

## 📦 Requirements

Install the required dependencies:
```
pip install torch torchvision numpy pandas matplotlib pillow scikit-learn
```
---

## 📊 Dataset

### Global Wheat Detection Dataset

- High-resolution RGB field images  
- Annotations provided in CSV format  
- Each annotation contains bounding box coordinates for wheat heads  

Bounding box format:

x_min, y_min, width, height  

Converted internally to:

[x1, y1, x2, y2]

---

## 🏗 Model Architecture

### Base Model
- Faster R-CNN  
- ResNet50 backbone (ImageNet pretrained)  
- Feature Pyramid Network (FPN)  

### Detection Head
- Region Proposal Network (RPN)  
- Classification head  
- Bounding box regression head  

This is a **two-stage object detector** optimized for accurate localization.

---

## 🔄 Data Preprocessing

- Load images using PIL  
- Parse CSV annotations  
- Convert bounding box format  
- Normalize images  
- Train–validation split  

---

## 🚀 Training Configuration

- Framework: PyTorch  
- Optimizer: SGD / Adam  
- Loss:
  - Classification loss  
  - Bounding box regression loss  

Training loop example:

model.train()  
loss = sum(loss for loss in loss_dict.values())  
loss.backward()  
optimizer.step()  

---

## 🧪 Prediction & Evaluation

- Predict bounding boxes and confidence scores  
- Visualize predictions on images  
- Qualitative evaluation through visual inspection  

---

## 🖼 Detection Results

Below are sample outputs from the trained Faster R-CNN model.  
Red bounding boxes indicate **detected wheat heads**.


### 📍 Sample Result 1
<img width="512" height="512" alt="result_1" src="https://github.com/user-attachments/assets/6e8634e1-e1e4-46f9-99f9-4bb807f091e8" />

### 📍 Sample Result 2
<img width="512" height="512" alt="result_2" src="https://github.com/user-attachments/assets/b71b758b-6d1e-4e76-94ff-abef450c4472" />

### 📍 Sample Result 3
<img width="512" height="512" alt="result_3" src="https://github.com/user-attachments/assets/3ba3b794-90e3-4a48-ae26-e85018d62c43" />

### 📍 Sample Result 4
<img width="512" height="512" alt="result_4" src="https://github.com/user-attachments/assets/3553da5a-0b30-45d1-bf82-e27b036f7bd8" />

---

## ⚠ Notes

- Dataset images vary in lighting and scale  
- Performance depends on annotation quality  
- No mAP metric calculated (visual evaluation only)  

---

## 🔮 Future Improvements

- Data augmentation  
- mAP-based evaluation  
- Longer training schedules  
- Model export (ONNX / TorchScript)  
- Deployment using Streamlit or FastAPI  

---

## 👨‍💻 Author

Rushikesh Raghatate  
Computer Science | Deep Learning | Computer Vision  
