**Project Title: Image Classification with CNNs**

---

### Objective:

Build a Convolutional Neural Network (CNN) to classify images from one of the following datasets:

- CIFAR-100
- Fashion MNIST
- MNIST
- Cats vs Dogs

You are free to choose any one dataset that interests you. The goal is to understand CNN architecture, data preprocessing, model training, and evaluation.

---

### Dataset Import Statements

Choose your dataset and use one of the following code snippets:

#### CIFAR-100 (TensorFlow)

```python
from tensorflow.keras.datasets import cifar100
(x_train, y_train), (x_test, y_test) = cifar100.load_data(label_mode='fine')
```

#### Fashion MNIST (TensorFlow)

```python
from tensorflow.keras.datasets import fashion_mnist
(x_train, y_train), (x_test, y_test) = fashion_mnist.load_data()
```

#### MNIST (TensorFlow)

```python
from tensorflow.keras.datasets import mnist
(x_train, y_train), (x_test, y_test) = mnist.load_data()
```

#### Cats vs Dogs (TensorFlow Datasets)

```python
import tensorflow_datasets as tfds
(ds_train, ds_test), ds_info = tfds.load(
    'cats_vs_dogs',
    split=['train[:80%]', 'train[80%:]'],
    with_info=True,
    as_supervised=True
)
```

---

### Task Breakdown:

1. Import and visualize the dataset

   - Display a few sample images with their labels

2. Preprocess the data

   - Normalize pixel values (0 to 1)
   - Reshape if necessary (especially grayscale images)
   - Convert labels to categorical if required

3. Design and implement a CNN model

   - Use Conv2D, MaxPooling2D, Flatten, Dense layers
   - Use ReLU activation and softmax at the output
   - Use dropout (optional)

4. Compile the model

   - Optimizer: Adam
   - Loss function: Categorical or sparse categorical crossentropy (depending on label encoding)
   - Metric: Accuracy

5. Train the model

   - Train for at least 10 epochs
   - Plot training and validation accuracy and loss

6. Evaluate the model

   - Use the test dataset
   - Display accuracy and confusion matrix

7. Optional (Bonus)

   - Try data augmentation using ImageDataGenerator
   - Save the model using model.save()

---

### Final Deliverables

- Python Notebook file with:
  - Code for each step
  - Proper comments and markdown cells
  - Results and plots
  - Screenshot or explanation of the confusion matrix- Short reflection (5-6 lines): What you learned, what was challenging
- PowerPoint Presentation
- 2-Pager Summary report 
---

### Deadline:

Submit your completed notebook by: April 28th 2025

---

### Submission:

Upload your `.ipynb` file or `.zip` with `.py` file and assets to classes.pace.edu 

End of instructions.

