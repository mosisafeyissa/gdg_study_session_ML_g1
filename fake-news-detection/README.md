
#  Fake News Detection Using Neural Network

## Task Overview

This project is a **Fake News Detection system** built using a **Neural Network**. The model classifies news headlines as either **Fake News** or **Real News**.

---

## Dataset

The dataset used in this project contains two columns:

* **text** → News headline
* **label** → Target value

  * `0` → Real News
  * `1` → Fake News

---

## Technologies Used

* Python
* Pandas
* Scikit-learn
* TensorFlow / Keras

---

##  Project Workflow

### 1. Data Loading

The dataset is loaded using Pandas and explored to understand the distribution of fake vs real news.

### 2. Text Preprocessing

Text data is converted into numerical format using **TF-IDF Vectorization**.

### 3. Train-Test Split

The dataset is split into:

* 80% Training Data
* 20% Testing Data

### 4. Neural Network Model

A **Feedforward Neural Network** was built with the following structure:

* Input Layer
* Hidden Layer (128 neurons, ReLU)
* Hidden Layer (64 neurons, ReLU)
* Output Layer (1 neuron, Sigmoid)

### 5. Model Training

* Optimizer: Adam
* Loss Function: Binary Crossentropy
* Epochs: 15
* Batch Size: 32

### 6. Model Evaluation

The model is evaluated using accuracy on the test dataset.

---

##  Results

* **Test Accuracy:** 80%  


##  Model

The trained model is saved as:

fake_news_model.keras

---

##  How to Run the Project

1. Clone the repository:

```
git clone https://github.com/mosisafeyissa/fake-news-detection.git
```

2. Install dependencies:

```
pip install pandas scikit-learn tensorflow
```

3. Run the notebook or Python script.
