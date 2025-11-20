# Handwritten Letter Classifier (A-Z)
This project is a **Convolutional Neural Network (CNN)** that classifies handwritten letters (A-Z), inspired by the EMNIST Letters dataset. Users can draw a letter on a Tkinter canvas and the model predicts the corresponding letter.

## Features
* Train a CNN to classify handwritten letters.
* Real-time drawing interface using **Tkinter**.
* Data augmentation using ```ImageDataGenerator``` for better generalization.
* Save and load trained models for instant predictions.
* Accuracy and loss visualization using **Matplotlib**.

## Repository Structure
```
handwritten-letter-classifier/
├─ emnist-letters-train-images-idx3-ubyte
├─ emnist-letters-train-labels-idx1-ubyte
├─ emnist-letters-test-images-idx3-ubyte
├─ emnist-letters-test-labels-idx1-ubyte
├─ letter_model.keras
├─ letter_classifier.py
├─ train_model.ipynb
└─ README.md
```

## Requirements
Python 3.8+ with the following libraries:
* [tensorflow](https://www.tensorflow.org/keras)
* [numpy](https://numpy.org/)
* [idx2numpy](https://pypi.org/project/idx2numpy/)
* [matplotlib](https://matplotlib.org/)
* [Pillow](https://pillow.readthedocs.io/)
* [Tkinter](https://docs.python.org/3/library/tkinter.html) (usually comes with Python)

Install dependencies via pip:
``` bash
pip install tensorflow numpy idx2numpy matplotlib pillow
```

## Getting Started
**1. Clone the repository**
``` bash
git clone https://github.com/MaryvilleUniversity-AI/handwritten-letter-classifier.git
cd handwritten-letter-classifier
```

**2. Download the EMNIST Letters Dataset**
Download from [EMNIST dataset](https://www.nist.gov/itl/products-and-services/emnist-dataset) and place the following files in the repo root:
* ```emnist-letters-train-images-idx3-ubyte```
* ```emnist-letters-train-labels-idx1-ubyte```
* ```emnist-letters-test-images-idx3-ubyte```
* ```emnist-letters-test-labels-idx1-ubyte```

**3. Train the Model (Optional)**
If you want to retrain the model:
``` bash
jupter notebook train_model.ipynb
```
This will:
* Load and preprocess the EMNIST letters dataset.
* Train a CNN with data augmentation.
* Save the trained model as ```letter_model.keras```.

**4. Run the Tkinter GUI**
```bash
python letter_classifier.py
```
* Draw a letter on the canvas.
* Click **Predict** to see the model's prediction.
* Click **Clear** to draw a new letter.

## Model Performance
* **Final Accuracy:** ~95% on EMNIST Letters test set.
* **Data Augmentation:** Small rotations, width/height shifts to improve generalization.

## Notes
* The model may confuse visually similar letters (eg., ``b`` vs ``d``, ``p`` vs ``q``).
* Avoid flipping the images during preprocessing, as it can confuse the network.

## References
* EMNIST Dataset: https://www.nist.gov/itl/products-and-services/emnist-dataset
* Keras Documentation: https://www.tensorflow.org/keras
* Tkinter Documentation: https://docs.python.org/3/library/tkinter.html

## Example Output

![Example Drawing](assets/example_output.png)
