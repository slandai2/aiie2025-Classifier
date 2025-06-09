 ## Overview
 Image classification is an incredibly useful tool in regards to identifying small details or changes in previously existing data. Convolutional Neural Networks (CNNs) are sets of different forms of layers that learn image features and classify them according to a dataset. The combination of convolutional, max pooling, flatten, and dense layers are used to search through image data and connect their previously existing neurons to predict the classificaiton of a given image. For our classification model, our team decided on chihuahuas and muffins.

 
![muffin-meme2](https://github.com/user-attachments/assets/cea2d46a-9d9b-47ef-8331-0bfe0209f60a)

 Our team imported an existing dataset from Kaggle that contained testing and training datasets for muffins and chihuahuas. The dataset was defined to a path and local path. The images from said dataset were resized to a consistent height and width before being placed into a separate dataset. 

 We then imported TensorFlow to assist in the idenification process. Two directories were created for testing and training our data. We then defined our image data generator before loading the data. We went on to build our sequential model through several Rectified Linear Unit layers and converted our classes into binary. We compiled our data and ran it through 8 epochs for 90% accuracy. 

 ![Untitled](https://github.com/user-attachments/assets/c18c3d86-d3f7-47cd-afca-f756671a36b4)

