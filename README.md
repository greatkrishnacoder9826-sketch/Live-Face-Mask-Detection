# 😷 Live Face Mask Detection 

> A real-time computer vision project that detects whether a person is wearing a face mask or not using a webcam. Built with TensorFlow/Keras and OpenCV.

## 📖 Table of Contents
* [About the Project](#about-the-project)
* [Features](#features)
* [Technologies Built With](#technologies-built-with)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Project Structure](#project-structure)
* [Usage](#usage)
* [Contributing](#contributing)

---

## 💡 About the Project

In the wake of global health concerns, wearing face masks has become a vital safety measure. This project automates the detection of face masks in real-time. It uses a deep learning model trained on a custom dataset of images (Mask vs. No Mask) and integrates with OpenCV to draw bounding boxes and labels around detected faces via a live webcam feed. 

It also automatically captures and sorts the detected faces into respective folders (`faces/with_mask` and `faces/without_mask`) for further review or training!

## ✨ Features

* **Data Augmentation:** Uses TensorFlow's `ImageDataGenerator` to artificially expand the training dataset (rotation, zooming, shifting, flipping) for a more robust model.
* **Real-time Detection:** Captures live video feed using OpenCV and performs mask detection on the fly.
* **Auto-Categorization:** Automatically crops and saves detected faces into specific directories based on their classification (Mask / No Mask).
* **Clear Visual Cues:** Displays bounding boxes around faces—Green for "Mask" and Red for "No Mask".

## 🛠️ Technologies Built With

* [Python](https://www.python.org/)
* [TensorFlow / Keras](https://www.tensorflow.org/) (for training the Deep Learning CNN model)
* [OpenCV](https://opencv.org/) (for real-time webcam rendering and face detection)
* [Matplotlib](https://matplotlib.org/) (for data visualization)

---

## 🚀 Getting Started

Follow these steps to set up the project on your local machine.

### Prerequisites
Make sure you have Python 3.x installed. You will also need to install the required Python libraries:
```sh
pip install tensorflow opencv-python matplotlib jupyter notebook
Installation
Clone the repository:

Bash
git clone [https://github.com/your-username/face-mask-detection.git](https://github.com/your-username/face-mask-detection.git)
cd face-mask-detection
Prepare your dataset:

Ensure you have your training and validation images inside the train and valid folders respectively.

Inside these folders, there should be two sub-directories: one for mask images and one for no-mask images.

Open the Jupyter Notebook:

Bash
jupyter notebook "detect_fixed (2).ipynb"
📂 Project Structure
When you run the notebook, it will automatically set up the following directory structure for you:

Plaintext
├── train/                  # Training data
├── valid/                  # Validation data
├── model/                  # Directory to save the final trained model
├── models/                 # Directory to save model checkpoints
├── faces/                  # Directory where real-time captures are saved
│   ├── with_mask/          # Saved faces detected WITH a mask
│   └── without_mask/       # Saved faces detected WITHOUT a mask
└── detect_fixed (2).ipynb  # Main Jupyter Notebook
🎮 Usage
Open the notebook and run the cells step-by-step.

The initial cells will augment the data and train the categorical model (Mask: 0, No Mask: 1).

Once the model is trained, execute the OpenCV cell to launch the live webcam feed.

Put on a mask (or take it off) to see the real-time detection in action!

Press the Q key on your keyboard to stop the live webcam feed and close the window safely.

🤝 Contributing
Contributions, issues, and feature requests are welcome!
