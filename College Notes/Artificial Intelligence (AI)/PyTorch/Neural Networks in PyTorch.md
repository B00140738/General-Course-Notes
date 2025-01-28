# Creating a Neural Network in PyTorch

This note outlines how to create a flexible neural network class in PyTorch and provides detailed explanations for each parameter used in the model definition.

---

## **1. Neural Network Class**

```python
import torch
import torch.nn as nn

class NeuralNetwork(nn.Module):
    def __init__(self, input_size, output_size, hidden_layers=None, activation=nn.ReLU, dropout=0.0):
        super(NeuralNetwork, self).__init__()
        
        layers = []
        all_layers = [input_size] + (hidden_layers or []) + [output_size]
        for i in range(len(all_layers) - 1):
            layers.append(nn.Linear(all_layers[i], all_layers[i + 1]))
            if i < len(all_layers) - 2:  # No activation/dropout on the output layer
                layers.append(activation())
                if dropout > 0:
                    layers.append(nn.Dropout(dropout))
        
        self.network = nn.Sequential(*layers)

    def forward(self, x):
        return self.network(x)
```

---

## **2. Parameters Explained**

### **`self`**

- **Description**: Refers to the instance of the class itself.
- **Purpose**: Used to access attributes and methods of the class.

---

### **`input_size`**

- **Type**: `int`
- **Description**: Number of features in the input data (i.e., the size of the input layer).
- **Example**: For an MNIST image with 28x28 pixels, `input_size` = 784.

---

### **`output_size`**

- **Type**: `int`
- **Description**: Number of output neurons, typically corresponding to the number of classes or regression targets.
- **Example**: For a 10-class classification problem, `output_size` = 10.

---

### **`hidden_layers`**

- **Type**: `list of int` or `None`
- **Description**: A list where each element represents the number of neurons in a hidden layer. If `None`, the network will only have input and output layers.
- **Default**: `None`
- **Example**: `hidden_layers=[128, 64]` creates two hidden layers with 128 and 64 neurons, respectively.

---

### **`activation`**

- **Type**: Callable (e.g., `nn.ReLU`, `nn.Sigmoid`, etc.)
- **Description**: Activation function applied to the outputs of each hidden layer.
- **Default**: `nn.ReLU`
- **Example**:
    - Use `nn.ReLU` for a rectified linear unit activation.
    - Use `nn.Sigmoid` for sigmoid activation if required.

---

### **`dropout`**

- **Type**: `float`
- **Description**: Dropout rate to apply during training, which randomly sets a fraction of neurons to 0 to prevent overfitting.
- **Default**: `0.0` (no dropout).
- **Range**: `0.0` to `1.0`
- **Example**: `dropout=0.2` drops 20% of neurons during training.

---

## **3. Example Usage**

```python
# Define the model
input_size = 784  # 28x28 images
output_size = 10  # 10 classes
hidden_layers = [128, 64]
activation = nn.ReLU

dropout = 0.2

model = NeuralNetwork(input_size, output_size, hidden_layers, activation, dropout)

print(model)
```

---

## **4. Key Notes**

- **Scalability**: The class is designed to handle arbitrary hidden layers.
- **Modularity**: You can easily change the activation function or add dropout.
- **Forward Pass**: The `forward` method defines how data flows through the network.

---

## **5. Future Enhancements**

- Add methods for saving and loading the model.
- Integrate training and evaluation loops.
- Experiment with different optimizers and learning rate schedulers.

---

## **6. Related Resources**

- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [Neural Network Basics](https://en.wikipedia.org/wiki/Artificial_neural_network)