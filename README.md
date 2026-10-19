# CIFAR-10 Image Classification with CNN and MobileNetV2

An end-to-end computer vision portfolio project comparing convolutional neural networks (CNNs) and transfer learning on the CIFAR-10 image dataset.

## Project goals

- Explore and visualize image data and class distribution.
- Preprocess images and create a validation split.
- Train a basic CNN baseline.
- Train a CNN with data augmentation.
- Use ImageNet-pretrained MobileNetV2 for transfer learning.
- Fine-tune selected MobileNetV2 layers with a low learning rate.
- Evaluate models using accuracy, classification report, and confusion matrix.
- Compare model performance and save a trained model.

## Dataset

CIFAR-10 contains 60,000 32×32 RGB images across 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck. Keras downloads the dataset automatically when the notebook runs.

- Official dataset: https://www.cs.toronto.edu/~kriz/cifar.html
- TensorFlow tutorial: https://www.tensorflow.org/tutorials/images/cnn
- Keras transfer learning guide: https://keras.io/guides/transfer_learning/

## Run in Google Colab

1. Upload `CIFAR10_CNN_Image_Classification.ipynb` to Google Colab, or open it from your GitHub repository.
2. Select **Runtime → Change runtime type → T4 GPU** (if available).
3. Run the notebook cells from top to bottom.
4. The notebook downloads CIFAR-10 automatically. MobileNetV2 may also download ImageNet pretrained weights, so an internet connection is needed for the first run.
5. Review the model comparison table and confusion matrix. The notebook saves checkpoints and a final `.keras` model during execution.

## Models

| Model | Purpose |
|---|---|
| Basic CNN | Baseline convolutional neural network |
| Augmented CNN | Tests whether image augmentation improves generalization |
| MobileNetV2 (initial) | Transfer learning with a frozen pretrained backbone |
| MobileNetV2 (fine-tuned) | Fine-tunes the final pretrained layers on CIFAR-10 |

## Evaluation

The notebook reports test accuracy and loss, per-class precision/recall/F1-score, a confusion matrix, and an accuracy comparison chart. Actual results vary by environment and training run; no accuracy level is guaranteed. For rigorous experiments, choose models using validation metrics and evaluate the test set only once.

## Tools and skills

- Python, NumPy, pandas, Matplotlib, Seaborn
- TensorFlow / Keras
- CNN, image augmentation, transfer learning, fine-tuning
- Model evaluation and error analysis
- Google Colab with GPU acceleration

## Repository structure

```text
CIFAR10-CNN-Image-Classification/
├── CIFAR10_CNN_Image_Classification.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Requirements

Google Colab already provides most dependencies. For a local environment, install the packages listed in `requirements.txt`. A compatible TensorFlow installation and supported GPU setup are optional; CPU execution may be slower.

## License

This project notebook is provided for learning and portfolio use. Check the licenses of third-party libraries and dataset resources before redistribution.
