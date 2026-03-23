# Deep-Learning-Project

company name: CodeTech IT solutions

Name : Rajesh R

domain : Data Science

duration: 4 Weeks

Intern ID : CTIS6705

mentor : Neela Santosh

descrpition of the task :
This project demonstrates the implementation of a basic neural network model using PyTorch to classify handwritten digits from the MNIST dataset. The goal of this project is to train a model that can accurately recognize digits (0–9) based on image input.

The process begins with importing essential libraries such as Torch, Torchvision, and Matplotlib. Torch provides the framework for building and training neural networks, while Torchvision offers access to popular datasets like MNIST. Matplotlib is used for visualizing the training progress.

Next, the MNIST dataset is loaded using torchvision.datasets.MNIST. This dataset consists of grayscale images of handwritten digits, each of size 28×28 pixels. A transformation is applied using transforms.ToTensor(), which converts images into tensor format and scales pixel values between 0 and 1. The dataset is downloaded (if not already present) and stored locally.

To efficiently process the dataset, a DataLoader is created using torch.utils.data.DataLoader. This divides the dataset into smaller batches (batch size of 64) and shuffles the data to ensure randomness during training. Batching helps in faster computation and better generalization of the model.

The neural network model is defined using nn.Sequential, which allows stacking layers in a linear order. The model consists of:

A Flatten layer to convert the 28×28 image into a 1D vector of size 784.
A fully connected layer (Linear) with 128 neurons.
A ReLU activation function to introduce non-linearity.
A final Linear layer with 10 outputs, corresponding to the 10 digit classes.

The loss function used is CrossEntropyLoss, which is suitable for multi-class classification problems. It measures how well the predicted outputs match the actual labels. The optimizer chosen is Adam, a popular optimization algorithm known for its efficiency and adaptive learning rate. The learning rate is set to 0.001.

The training process runs for 3 epochs. In each epoch, the model processes all batches of training data. For each batch, the following steps are performed:

Gradients are reset using optimizer.zero_grad().
A forward pass is performed to compute predictions.
The loss is calculated using the loss function.
Backpropagation is performed using loss.backward() to compute gradients.
Model parameters are updated using optimizer.step().

The total loss for each epoch is accumulated and stored in a list. This helps in tracking how the model improves over time. After each epoch, the loss value is printed to monitor training progress.

Once training is complete, the loss values are plotted using Matplotlib. The graph shows how the loss decreases over epochs, indicating that the model is learning effectively.


Overall, this project provides a simple introduction to deep learning using PyTorch. It covers key concepts such as dataset loading, neural network design, training loops, loss functions, and performance visualization. This forms the foundation for building more complex models in real-world applications.

ouput of the task 


