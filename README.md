# Monocular-Depth-Estimation-with-Lightweight-CNN-and-Spatial-Attention

Monocular depth estimation from a single RGB image is a core challenge in computer vision with real-world applications in autonomous navigation, augmented reality, and robotics. This project explores how training hyperparameters influence the performance of a lightweight CNN-based encoder-decoder architecture with spatial attention, inspired by Monodepth2.

This repository houses two Jupyter notebooks on self-supervised monocular depth estimation hyperparameter tuning as "Digging Into Self-Supervised Monocular Depth Estimation" by Godard et al. (ICCV 2019).
The First notebook is an improvement code file, where we used the addition of the dataset to 10,000 samples and lowering epochs to 5 and 12 due to GPU limitations. We experimented with batch sizes of 8, 16, and 50 (the latter for 500 and 700 epochs only) and saw their impacts on convergence stability and prediction accuracy, further optimizing the training process.

The second notebook is a reference code file that was trained before trying 10,000 samples. It trains a light CNN-based encoder-decoder model (similar to Monodepth2) on 2000 samples with PyTorch, experiments at 100, 200, 500, and 700 epochs, with a constant learning rate of 0.1, and batch sizes 8, 16, and 50, with Adam and SGD optimizers.


## Requirements

- Python 3.8+
- Kaggle account + API token (`kaggle.json`) [username and key used for this project is attached in kaggle.json file]
- `kaggle`, `torch`, `torchvision`, `matplotlib`, `numpy`, `pandas` (installed via pip)

---

## How to Run on Google Colab (Recommended to Leverage Colab’s GPU)

1. Go to [Google Colab](https://colab.research.google.com/).
2. Upload the notebook for ex.`Reference_code_2000.ipynb`.
3. Upload your `kaggle.json` file when prompted.
   - Get it from: [https://www.kaggle.com/](https://www.kaggle.com/) → "Log in" → "Go to your profile" → "Settings" → "Create New API Token" (A .json file will be downloaded with the key)
   - or use the kaggle.json attached.
4. Run all cells (`Runtime > Run all`).
5. Connect to T4 GPU while running the code. (Its advised to run this code in Colab itself due to GPU requirement)

## How to Run Locally

1. Download the notebook.
2. Place your `kaggle.json` in the same folder as the notebook.
3. Install required packages:
4. Run all cells.

-------------------------------------------------------------------------------------------------------
Note: This project is for educational purposes.



