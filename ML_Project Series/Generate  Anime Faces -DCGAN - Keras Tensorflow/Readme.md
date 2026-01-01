# **Deep Convolutional Generative Adversarial Network (DCGAN) for Image Generation**

This project implements a **Deep Convolutional Generative Adversarial Network (DCGAN)** to generate high-quality synthetic images from random noise. The DCGAN framework consists of two core components:

1. **Generator:** A neural network designed to generate realistic images from random noise.
2. **Discriminator:** A neural network tasked with distinguishing between real images (from the dataset) and synthetic images created by the generator.

---

### **Key Features**
- **Custom Dataset Support:** Works seamlessly with user-defined datasets, such as anime images.
- **Modular Architecture:** Easily adjustable parameters, including latent dimensions, learning rates, and network layers.
- **Real-Time Visualization:** Displays generated images during training for progress tracking.
- **Model Checkpointing:** Periodically saves trained models and intermediate outputs for later use.

---

### **Workflow Overview**

#### **1. Dataset Preparation**
- Place your dataset in a directory and specify its path in the `BASE_DIR` variable.  
  Example:
  ```python
  BASE_DIR = 'C:/Users/ASUS/OneDrive/Desktop/Python_Course/data'
  ```
- Dataset preprocessing includes resizing images to 64x64 pixels, reshaping them, and normalizing pixel values for compatibility with the DCGAN model.

- **Visualize the Dataset:** The first image (below) displays a grid of 64 images from the dataset. This step helps verify that images are loaded correctly before training.  

  ![Dataset Visualization](https://github.com/user-attachments/assets/32d92a36-1a01-4608-84d6-116cfd125afa)

#### **2. Model Components**
- **Generator:** Takes random noise as input and outputs synthetic images. The second image (below) represents the architecture of the generator model, showcasing how it builds images layer by layer.  
![Screenshot 2024-11-29 131547](https://github.com/user-attachments/assets/04a9ae25-7da5-4128-a62d-bad475c82490)


- **Discriminator:** Evaluates the authenticity of images, determining whether they are real or generated. The third image (below) provides a detailed view of the discriminator model's structure.  

 ![Screenshot 2024-11-29 131557](https://github.com/user-attachments/assets/8a08ea54-1cda-47ff-97f2-3b968ff1f4f8)


#### **3. Training Process**
- Utilize the `DCGAN` class to train the model on your dataset.
- Track generator and discriminator losses during training.
- Save generated images and trained models after each epoch for evaluation.

- **Epoch 1 Output:** The fourth image (below) shows the generated images after completing the first training epoch. These images demonstrate the early stages of learning by the generator.  

![Screenshot 2024-11-29 132102](https://github.com/user-attachments/assets/bb22f26a-70e1-45ac-9ebb-633fded034c7)


Example training command:
```python
dcgan.fit(train_images, epochs=N_EPOCHS, callbacks=[DCGANMonitor()])
```

#### **4. Post-Training Image Generation**
After training, create new images with the generator:
```python
noise = tf.random.normal([1, 100])
g_img = dcgan.generator(noise)
plt.imshow(array_to_img(g_img[0]))
plt.axis('off')
plt.show()
```

---

### **Customizable Parameters**
1. **Latent Dimension (`LATENT_DIM`):** Adjust the input noise dimension to influence the complexity of generated images.
2. **Learning Rates:** Fine-tune learning rates for both the generator (`G_LR`) and discriminator (`D_LR`).
3. **Image Resolution:** Modify input shape and convolutional layers for generating higher-resolution images.

---

### **Outputs**
- Generated images saved during and after training (e.g., `epoch_001.png`, `epoch_002.png`).
- Final generator model (`generator.h5`) for generating images without retraining.

---

### **Additional Notes**
1. Install required dependencies using:
   ```bash
   pip install tensorflow numpy matplotlib tqdm
   ```
2. Visualize a grid of 64 images from the dataset to verify preprocessing before training.
3. Refer to this [dataset link](https://www.kaggle.com/datasets/soumikrakshit/anime-faces) for sample data.

---

### **Acknowledgments**
This implementation is inspired by foundational DCGAN architectures and leverages modern deep learning practices for realistic image generation.

Enjoy creating with DCGAN! 🎨

--- 

