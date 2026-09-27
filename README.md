# Handwritten Character Recognition

A deep learning project that recognizes handwritten digits using a Convolutional Neural Network (CNN).

## Project Overview

This project uses the MNIST handwritten digit dataset to build a CNN capable of classifying grayscale images of handwritten digits from 0 to 9.

The model processes 28×28 pixel images and predicts one of 10 digit classes.

## Dataset

The MNIST dataset contains:

- 60,000 training images
- 10,000 test images
- 10 classes (digits 0–9)
- 28×28 grayscale images

## Machine Learning Workflow

1. Load the MNIST dataset
2. Visualize sample handwritten digits
3. Normalize pixel values from 0–255 to 0–1
4. Add the grayscale channel dimension
5. Build a CNN
6. Compile the model
7. Train for 5 epochs
8. Evaluate on unseen test data
9. Generate predictions
10. Analyze the confusion matrix
11. Generate a classification report
12. Save the trained model

## CNN Architecture

The model contains:

- Input layer: 28×28×1
- Convolutional layer: 32 filters
- Max pooling
- Convolutional layer: 64 filters
- Max pooling
- Flatten layer
- Dense layer with 64 neurons
- Output layer with 10 neurons
- ReLU activation for hidden layers
- Softmax activation for the output layer

## Training Configuration

The model was trained using:

- Optimizer: Adam
- Loss function: Sparse Categorical Crossentropy
- Batch size: 64
- Epochs: 5
- Validation split: 10%

## Results

The trained CNN achieved:

| Metric | Result |
|---|---:|
| Test Accuracy | 99.05% |
| Test Loss | 0.0286 |
| Macro F1 Score | 99.04% |
| Weighted F1 Score | 99.05% |

The evaluation was performed on the 10,000-image MNIST test set.

## Evaluation

The project includes:

- Training and validation accuracy plot
- Training and validation loss plot
- Confusion matrix
- Classification report
- Sample prediction visualization

## Project Structure

```text
agenticx-handwritten-character/
│
├── data/
│
├── notebooks/
│   └── Handwritten_Character_Recognition.ipynb
│
├── outputs/
│   ├── sample_images.png
│   ├── training_history.png
│   ├── training_loss.png
│   ├── confusion_matrix.png
│   ├── predictions.png
│   └── model_metrics.csv
│
├── src/
│   └── mnist_cnn_model.keras
│
├── .gitignore
├── README.md
└── requirements.txt

How to Run
Create a virtual environment:
python -m venv .venv

Activate it on Windows Git Bash:
source .venv/Scripts/activate

Install dependencies:
pip install -r requirements.txt

Launch Jupyter:
jupyter notebook

Open:
notebooks/Handwritten_Character_Recognition.ipynb

Limitations
This model was trained and evaluated on the MNIST dataset. Its performance on handwritten characters from different datasets, writing styles, image sizes, or real-world conditions may differ.

Author
Jothi A

Built as part of the AgenticX internship.