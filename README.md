 ## Overview
 Image classification is an incredibly useful tool in regards to identifying small details or changes in previously existing data. Convolutional Neural Networks (CNNs) are sets of different forms of layers that learn image features and classify them according to a dataset. The combination of convolutional, max pooling, flatten, and dense layers are used to search through image data and connect their previously existing neurons to predict the classificaiton of a given image. For our classification model, our team decided on chihuahuas and muffins.

 
![muffin-meme2](https://github.com/user-attachments/assets/cea2d46a-9d9b-47ef-8331-0bfe0209f60a)


## Dataset information 

 Our team imported an existing dataset from Kaggle that contained testing and training datasets for muffins and chihuahuas. The dataset consists of 6,000 images of muffins and dogs.

```
import kagglehub
import shutil
import os

path = kagglehub.dataset_download("samuelcortinhas/muffin-vs-chihuahua-image-classification")
```

 
 *Dataset source: https://www.kaggle.com/datasets/samuelcortinhas/muffin-vs-chihuahua-image-classification/data*

### Dataset preprocessing 

 The dataset was defined to a path and local path. The images from said dataset were resized to a consistent height and width (256x256) before being placed into a separate dataset. 

 We then imported TensorFlow to assist in the idenification process. Two directories were created for testing and training our data. We then defined our image data generator before loading the data. We went on to build our sequential model through several Rectified Linear Unit layers and converted our classes into binary.

 ## Model

 We created a simple CNN model starting with 3 Convolutional Layers, each of them followed by Max Pooling Layers. After several convolutional and max pooling layers, a flatten layer was added. To help the model make decisions, we added a Dense layer with 512 neurons and ReLU activation, and finally a single output neuron with a sigmoid function — since we’re doing binary classification: muffin or chihuahua.
 
 <img width="917" alt="Screenshot 2025-06-09 at 2 22 18 PM" src="https://github.com/user-attachments/assets/1e8d1336-0903-447d-890f-9a2cb1176991" />


 ## Example Usage

 After training the model on a dataset of resized images, we tested it using images from the test set to see how well it performs on new, unseen data. As shown in the examples below, the model was able to accurately classify whether the input image was a muffin or a chihuahua, demonstrating that it successfully learned to recognize the visual patterns that separate the two.
 
 ![Untitled](https://github.com/user-attachments/assets/68867006-50a3-4e5d-ab17-5601b30e26e6)
 ![Untitled-1](https://github.com/user-attachments/assets/1a04cbea-c110-4f1d-9af1-ff0c95e57a19)

## Experimentation

Our initial experiment used 3 Convolutional Layers and trained the model for 7 epochs.
An epoch simply means that the model has seen the entire training dataset once. So when we say 7 epochs, it means the model went through the training data 7 times, learning a bit more each time.

Below are visualization of training plots:  

 ![Untitled](https://github.com/user-attachments/assets/c18c3d86-d3f7-47cd-afca-f756671a36b4)

 As the epochs go on, both accuracy lines trend upward, it means the model is learning from the data and improving over time. By the 7th epoch, both training and validation accuracy are close to 90%. Even though the validation loss fluctuates a bit (which is normal, but learning rate can be changed to avoid this), the general downward trend means the model is becoming more confident and accurate in its predictions.

### Experiments with parameters layers

