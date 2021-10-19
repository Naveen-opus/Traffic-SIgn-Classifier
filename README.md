# Traffic-Sign-Classifier
We can read and understand traffic signs using our model, which is a critical task for all autonomous vehicles.

# Dataset
For this project, we are using the public dataset available at Kaggle:  

https://www.kaggle.com/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign

The dataset contains more than 50,000 images of different traffic signs. It is further classified into 43 different classes. The dataset is quite varying, some of the classes have many images while some classes have few images. The size of the dataset is around 300 MB. The dataset has a train folder which contains images inside each class and a test folder which we will use for testing our model.

# Steps Followed:
Explore the dataset
Build a CNN model
Train and validate the model
Test the model with test dataset

# The architecture of our model is:
2 Conv2D layer (filter=32, kernel_size=(5,5), activation=”relu”)
MaxPool2D layer ( pool_size=(2,2))
Dropout layer (rate=0.25)
2 Conv2D layer (filter=64, kernel_size=(3,3), activation=”relu”)
MaxPool2D layer ( pool_size=(2,2))
Dropout layer (rate=0.25)
Flatten layer to squeeze the layers into 1 dimension
Dense Fully connected layer (256 nodes, activation=”relu”)
Dropout layer (rate=0.5)
Dense layer (43 nodes, activation=”softmax”)
We compile the model with Adam optimizer which performs well and loss is “categorical_crossentropy” because we have multiple classes to categorise.

# Accuracy and Loss Graph

![image](https://user-images.githubusercontent.com/62651885/137872029-3d60e4fe-1850-4203-b5ba-c4c4fe018f02.png)

## With GUI:
![image](https://user-images.githubusercontent.com/62651885/137879839-0c2126fc-1137-4001-b861-0183b89d93e6.png)


