# 🎨 Neural Style Transfer using TensorFlow (VGG19)

## 📌 Project Overview

This project implements **Neural Style Transfer (NST)** using a pre-trained **VGG19 deep learning model** in TensorFlow. The goal is to generate a new image by combining:

* The **content** of one image
* The **style** (texture, colors, patterns) of another image

The final output is a stylized image that visually blends both inputs.

---

## 🚀 Features

* Uses **pre-trained VGG19 (ImageNet weights)** for feature extraction
* Extracts **content and style representations** from different layers
* Applies **Gram Matrix** to capture artistic style
* Optimizes the image using **Gradient Descent**
* Generates and saves a **stylized output image**

---

## 📂 Dataset

This project uses images from a **Kaggle dataset**.

* **Content Image** → Defines the structure of the output
* **Style Image** → Defines the artistic appearance

📌 Example paths used:

```
/kaggle/input/style-transfer/content/content1.jpg
/kaggle/input/style-transfer/style/style1.jpg
```

You can replace these with any images of your choice.

---

## 🧠 Model Architecture

* **Base Model**: VGG19 (pre-trained on ImageNet)
* **Content Layer**: `block5_conv2`
* **Style Layers**:

  * block1_conv1
  * block2_conv1
  * block3_conv1
  * block4_conv1
  * block5_conv1

---

## ⚙️ How It Works

1. Load and preprocess content & style images
2. Pass images through VGG19 to extract features
3. Compute:

   * **Content Loss** → preserves structure
   * **Style Loss** → applies artistic features
4. Optimize the generated image using backpropagation
5. Output the final stylized image

---

## 📊 Loss Function

Total loss is calculated as:

```
Total Loss = Style Loss + Content Loss
```

* Style Weight = `1e-2`
* Content Weight = `1e4`

---

## 🏋️ Training Details

* Epochs: `10`
* Steps per epoch: `100`
* Optimizer: **Adam**

---

## 📸 Output

The model generates:

* Content Image
* Style Image
* Final Stylized Image

💾 Output file:

```
stylized_output.png
```

---

## 🛠️ Requirements

Install the following libraries:

```
tensorflow
numpy
matplotlib
pillow
```

---

## ▶️ How to Run

1. Upload dataset to Kaggle or local environment
2. Update image paths if needed
3. Run the script
4. View and download the stylized output image

---

## 📈 Future Improvements

* Implement **Fast Style Transfer (real-time)**
* Add **multiple style blending**
* Improve quality using **higher resolution images**
* Build a **web app interface (Flask/Streamlit)**

---

## 👩‍💻 Author

**Tanishq Tomar**
Field: AI/ML

---

## 📌 Conclusion

This project demonstrates how deep learning can be used for creative tasks by merging artistic styles with real-world images using neural networks.

---
