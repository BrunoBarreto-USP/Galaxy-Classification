# Galaxy-Classification

This project uses a Convolutional Neural Network (CNN) to classify images of galaxies from the Galaxy10 dataset. The model is built and trained in Python using TensorFlow/Keras and the astroNN library.

## Project Overview

The notebook (`galcla.ipynb`) demonstrates the complete process of:
1.  Loading the Galaxy10 dataset, which contains images of galaxies and their corresponding classification labels.
2.  Preprocessing the data, including the removal of one of the classes to adjust the problem's scope.
3.  Building a CNN model with Convolution, Batch Normalization, MaxPooling, and Dropout layers.
4.  Training the model with training and validation data.
5.  Evaluating the model's performance using metrics like accuracy, precision, recall, and F1-score, as well as a confusion matrix.

## Dataset: Galaxy10

The `Galaxy10_SDSS` dataset is loaded using the `astroNN` library. It originally has 10 distinct classes of galaxies. In this project, class 5 ("Disk, Edge-on, Boxy Bulge") was removed to focus on a 9-class classification.

The classes are:
- `0`: Disk, Face-on, No Spiral
- `1`: Smooth, Completely round
- `2`: Smooth, in-between round
- `3`: Smooth, Cigar shaped
- `4`: Disk, Edge-on, Rounded Bulge
- `5`: Disk, Edge-on, No Bulge
- `6`: Disk, Face-on, Tight Spiral
- `7`: Disk, Face-on, Medium Spiral
- `8`: Disk, Face-on, Loose Spiral

## Model Architecture

The model is a sequential CNN with the following architecture:

| Layer (Type)         | Output Shape   | Param #   |
| ---------------------|--------------- |---------- |
| Conv2D               | (69, 69, 48)   | 1,344     |
| BatchNormalization   | (69, 69, 48)   | 192       |
| MaxPooling2D         | (34, 34, 48)   | 0         |
| ... (and so on) ...  | ...            | ...       |
| Dense (Output)       | (9)            | 585       |

**Total params:** 1,162,185

## Results

The final model achieved a **test accuracy of approximately 81.20%**.

## How to Use

1.  **Clone the repository:**
    ```bash
    git clone <YOUR_REPOSITORY_URL>
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run the notebook:**
    Open and run `galcla.ipynb` in a Jupyter environment (like Jupyter Lab or Google Colab).
