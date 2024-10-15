# Credit Card Reader and Dataset Augmentation

This project focuses on reading credit card images using OpenCV and augmenting the dataset for machine learning purposes. The images are processed using thresholding techniques and then organized into training and testing directories to create a robust dataset for future classification models.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview
This project helps in creating an augmented dataset of credit card images. It applies image processing techniques to preprocess the images and then augments the dataset by creating directories for training and testing. The goal is to build a large enough dataset for developing robust models for OCR (Optical Character Recognition) or credit card digit classification.

## Dataset
The dataset is created from two sample images of credit card digits. You can augment the dataset by generating different variations of the images (e.g., using OpenCV transformations).

## Installation
To run this project locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/n7kadda/Credit_card_reader.git
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Ensure you have OpenCV installed, as it's the primary library used for image processing:
    ```bash
    pip install opencv-python
    ```

4. You may need to modify the paths to your own dataset in the code to ensure the images are correctly read from your local system.

## Usage
1. Run the notebook or the Python scripts to load the credit card images, preprocess them, and organize them into datasets.
2. Example usage for loading and preprocessing the images:
    ```python
    import cv2

    # Load an image
    img = cv2.imread("path_to_image", 0)

    # Preprocess the image using thresholding
    _, thresholded = cv2.threshold(img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

    # Display the image
    cv2.imshow("Thresholded Image", thresholded)
    cv2.waitKey(0)
    ```

3. The dataset will be split into `train` and `test` directories based on digits found in the images.

## Results
This project creates directories containing preprocessed images of credit card digits. These images can be further used to train machine learning models for digit classification or optical character recognition (OCR).

## Contributing
Contributions are welcome! Please submit a pull request or open an issue to suggest improvements.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
