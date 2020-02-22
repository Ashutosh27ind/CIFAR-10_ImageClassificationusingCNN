# CIFAR-10_ImageClassificationusingCNN
In this project we will build multiple CNN models for **CIFAR-10** Image Classification on GPUs.

## Platform used :
https://www.nimblebox.ai/  
(_Enables working faster on AI Projects using power of high performance GPUs)

To build and train various CNN networks on the **CIFAR-10** dataset. It has 10 classes of 60,000 RGB images each of size (32, 32, 3). The 10 classes are aeroplane, automobile, bird, cat, deer, dog, frog, horse, ship and truck.

## CIFAR-10 Experiments  
In the coming few lectures, you will experiment with some hyperparameters and architectures and draw insights from the results. Some hyperparameters we will play with are:  
•	Adding and removing dropouts in convolutional layers  
•	Batch Normalization (BN)  
•	L2 regularisation  
•	Increasing the number of convolution layers  
•	Increasing the number of filters in certain layers     

There are separate ipynb files available for each of these experiments.  
 
### Experiment - I: Using dropouts after conv and FC layers  
In the first experiment, we will use dropouts both after the convolutional and fully connected layers. 
The results of the experiment are as follows:    
•	Training accuracy =  84%, validation accuracy = 79%

### Experiment - II: Remove the dropouts after the convolutional layers (but retain them in the FC layer). Also, use batch normalization after every convolutional layer.    
In the experiment 2 there is very high training accuracy and lower validation accuracy because we have removed the dropouts and hence overfitting has happened here  

### Experiment - III: Use batch normalization and dropouts after every convolutional layer. Also, retain the dropouts in the FC layer.  
The training accuracy has gone down because we have included the dropouts but it has not gone down too bad either. But the gap between training and validation accuracy is closed in so it is a generisable model.   

### Experiment - IV: Remove the dropouts after the convolutional layers and use L2 regularization in the FC layer. Retain the dropouts in FC.  
The result is worse overfitting again happened, the L2 regularisation is not that effective as the droputs. L2 regularisation is trying to keep the value of the weights down but seems to be too much of redundant connections and dropouts are throwing away such connections.  
### Experiment-V: Dropouts after conv layer, L2 in FC, use BN after convolutional layer  

### Experiment-VI: Add a new convolutional layer to the network. 
Note that by a 'convolutional layer',we are referring to a convolutional unit with two sets of Conv2D layers with 128 filters each (we are abusing the terminology a bit here).   

### Experiment - VII: Add more feature maps to the conv layers: from 32 to 64 and 64 to 128.    

## Result of the experiments:  
  
### Experiment - I (Use dropouts after conv and FC layers, no BN):   
o	Training accuracy =  84%, validation accuracy  =  79%  
### Experiment - II (Remove dropouts from conv layers, retain dropouts in FC, use BN):   
o	Training accuracy =  98%, validation accuracy  =  79%  
### Experiment - III (Use dropouts after conv and FC layers, use BN):  
o	Training accuracy =  89%, validation accuracy  =  82%  
### Experiment - IV (Remove dropouts from conv layers, use L2 + dropouts in FC, use BN):  
o	Training accuracy = 94%, validation accuracy = 76%.   
### Experiment-V: Dropouts after conv layer, L2 in FC, use BN after convolutional layer  
•	Train accuracy =  86%, validation accuracy = 83%  
### Experiment-VI: Add a new convolutional layer to the network  
•	Train accuracy =  89%, validation accuracy = 84%  
### Experiment-VII: Add more feature maps to the convolutional layers to the network  
•	Train accuracy =  92%, validation accuracy = 84%  

Based on these experiments, we saw that the performance of CNNs depends heavily on multiple hyperparameters - the number of layers, number of feature maps in each layer, the use of dropouts, batch normalisation, etc. Thus, it is advisable to first fine-tune your model hyperparameters by conducting lots of experiments. Only when you are convinced that you have found the right set of hyperparameters you should train the model with a larger number of epochs (since almost always the amount of time and computing power you have is limited).








