# 👚🧠 Fashion Classification using Neural Networks (Keras)

A beginner-friendly deep learning project that classifies fashion items using a simple neural network built with **Keras** and trained on the **Fashion MNIST dataset**.

---

## 🧾 Project Overview

The goal is to classify grayscale images of clothing into one of the following 10 categories:

| Label | Class        |
|-------|--------------|
| 0     | T-shirt/top  |
| 1     | Trouser      |
| 2     | Pullover     |
| 3     | Dress        |
| 4     | Coat         |
| 5     | Sandal       |
| 6     | Shirt        |
| 7     | Sneaker      |
| 8     | Bag          |
| 9     | Ankle boot   |

---

## 🧠 How It Works

### 1. **Dataset Loading**
- Loads the **Fashion MNIST dataset** from `keras.datasets`.
- The dataset contains 60,000 training and 10,000 test 28x28 grayscale images.

### 2. **Visualization**
- Sample images from the dataset are visualized using `matplotlib`.

### 3. **Data Preprocessing**
- Normalizes pixel values by scaling them between 0 and 1.

### 4. **Model Architecture**
A simple neural network built using `keras.Sequential`:
```python
model = keras.models.Sequential([
    keras.layers.Flatten(input_shape=(28, 28)),
    keras.layers.Dense(units=32, activation='relu'),
    keras.layers.Dense(units=10, activation='softmax')
])
