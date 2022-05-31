### Samsung Innovation Campus AI_Sign_MNIST Project

# Sign Language Detection

## Team: Vision of Sauron

- Abel Asfaw
- Hilarion Reyes
- Mosunmola Oyeleye
- Mya Thanegi Soe
- Giovan Panzanella

#### ================
### Table of Contents:
- Problem Definition
- Dataset Overview
- EDA
- Models
- Further Improvements
- Conclusion

<br>
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture1.png' width=80%> 

### Problem Definition:
- The deaf or people with hearing problems don’t have efficient applications that can be used to communicate
- Current visual recognition algorithms have issues with real world application
- American Sign Language is a complex language and primary language for deaf people.

<br> 
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture2.png' width=80%> 

### Dataset Overview:
- Training and test set contain a label ( 0-25) and letters (A-Z)
- Match the patterns of the MNIST dataset
- Each pixel is of size 28*28
- Each sample has 784 pixels

<br>
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture3.png' width=75%>

### Exploratory Data Analysis:
- Label Count ( How many times each letter appears)
- 0 – 25 is mapped to A-Z
- J and Z require motion
- There is no count for 9 = J and 25 = Z
- Highest count is Q

<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture4.png' width=75%>

### Dataset Image Previews:
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture5.png'>

## Models:
### Model 1: Stochastic Gradient Descent Architecture
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture6.png' width=60%>

- Built a custom SGD model using Convolution2D Layers and Dense Layers with a total of 1,526,425 trainable params.
- Used Max-pooling, Dropout, and Decay for Regularization..

#### Model 1: SGD Results
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture7.png' width=60%>
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture8.png' width=75%>

### Model 2: Pretrained ResNET Model 
- Introduced by Microsoft Research 
- Increasing network depth does not work by simply stacking layers together.
- applies concept of skip connection
- avoid small gradients by allowing this alternate shortcut path for gradient to flow through
- recommended to have a minimum shape of 32,32, (+ #of feature channels)
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture9.png' width=75%>

#### Model 2: ResNET Architecture
<div>
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture10.png' width=40%>
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture11.png' width=40%>
</div>

### Model 3: Custom Model RMSprop CNN
- most commonly applied to analyze visual imagery
- CNNs are regularized versions of multilayer perceptrons. 
- Multilayer perceptrons usually mean fully connected networks. 
- Each neuron in one layer is connected to all neurons in the next layer.
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture12.png' width=70%>

## Model 2 + 3: Results
<img src='https://github.com/Jamswhat2/SamsungInnovationAI_Sign_MNIST/blob/main/project_folder/Picture13.png' width=95%>
