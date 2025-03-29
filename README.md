# 🚀 Autoencoder for MNIST Digit Recognition

## 📌 Overview
This project implements an **autoencoder** using **PyTorch** to reconstruct handwritten digits from the MNIST dataset. The model consists of an **encoder-decoder architecture** with convolutional layers, batch normalization, dropout, and fully connected layers to improve learning and generalization.

## ✨ Features
✅ **Autoencoder Architecture:** Uses convolutional layers for feature extraction and transposed convolution for reconstruction.
✅ **Data Preprocessing:** Normalizes pixel values to the range [0,1] and reshapes images to (1, 28, 28).
✅ **GPU Support:** Automatically detects and utilizes GPU for training if available.
✅ **Visualization:** Displays original and reconstructed images after training.

## ⚙️ Installation
### 📋 Requirements
Ensure you have the following installed:
- 🐍 **Python 3.7+**
- 🔥 **PyTorch**
- 🗃️ **pandas**
- 📊 **matplotlib**

### 🛠️ Setup
Clone this repository and install dependencies:
```sh
$ git clone https://github.com/your-repo/autoencoder-mnist.git
$ cd autoencoder-mnist
$ pip install -r requirements.txt
```

## 🚀 Usage
### 🏋️ Training the Autoencoder
1. 📥 Download the MNIST dataset from Kaggle.
2. ✏️ Modify `file_path` in the script to point to the dataset.
3. ▶️ Run the script:
   ```sh
   python train_autoencoder.py
   ```

### 📸 Visualizing Results
After training, reconstructed images will be displayed to evaluate the performance.

## 🏗️ Model Architecture
### 🔷 Encoder
- 🏗️ **Conv2d (1 -> 32) + ReLU + BatchNorm**
- 🏗️ **Conv2d (32 -> 64) + ReLU + BatchNorm**
- 🔄 **Flatten + Fully Connected (64*7*7 -> 128) + Dropout**

### 🔶 Decoder
- 🔄 **Fully Connected (128 -> 64*7*7) + BatchNorm**
- 🔄 **ConvTranspose2d (64 -> 32) + ReLU + BatchNorm**
- 🔄 **ConvTranspose2d (32 -> 1) + Sigmoid**

## 📊 Results
The model progressively learns to reconstruct the MNIST digits, with the **Mean Squared Error loss decreasing** over **30 epochs** 📉.

## 🙌 Acknowledgments
- 📜 MNIST dataset from **Kaggle**.
- 📚 PyTorch documentation for deep learning implementation.

## 📜 License
This project is licensed under the **MIT License** 📄.

