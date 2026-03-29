This project is based on the work by AaravJoshi03.  
Modified, improved, and implemented by Anmol Choudhary.
# Face Mask Detection

A real-time face mask detection system using MobileNetV2 and OpenCV that detects whether a person is wearing a face mask or not through a webcam feed.

## Project Overview

This project uses deep learning and computer vision techniques to classify faces as either "With Mask" or "Without Mask" in real-time using a webcam. It achieves 99% accuracy on the test dataset.

## Tech Stack

- Python 3.11
- TensorFlow 2.21
- Keras
- OpenCV 4.13
- MobileNetV2 (Transfer Learning)
- scikit-learn
- NumPy
- Matplotlib

## Dataset

- Source: [Face Mask Dataset - Kaggle](https://www.kaggle.com/datasets/omkargurav/face-mask-dataset)
- 3725 images with mask
- 3828 images without mask
- Total: 7553 images

## Project Structure
```
face-mask-detection/
├── data/
│   ├── with_mask/
│   └── without_mask/
├── face_detector/
│   ├── deploy.prototxt
│   └── res10_300x300_ssd_iter_140000.caffemodel
├── train.py
├── detect.py
├── requirements.txt
└── README.md
```


## How to Run
### Train the model
```
python train.py
```
This will train the model and save it as `mask_detector.keras`

### Run real-time detection
```
python detect.py
```
This opens your webcam. Press `Q` to quit.

## Results

- Training Accuracy: 99%
- Validation Accuracy: 98.8%
- Test Accuracy: 99%

## How It Works

1. Faces are detected in each webcam frame using OpenCV's DNN face detector
2. Each detected face is passed through the trained MobileNetV2 model
3. The model predicts whether the person is wearing a mask or not
4. A green box appears for mask, red box for no mask with confidence percentage
## Installation & Setup

1. Clone the repository:
```
git clone https://github.com/anmol20c/face-mask-detection.git
cd face-mask-detection
```

2. Install dependencies:
```
pip install -r requirements.txt
```

3. Run the training script (optional):
```
python train.py
```

4. Run the detection system:
```
python detect.py
```

## Requirements
- Python 3.8+
- OpenCV
- TensorFlow / Keras
