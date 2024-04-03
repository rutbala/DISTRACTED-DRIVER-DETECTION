# DISTRACTED-DRIVER-DETECTION

Introduction:-

In this project, I developed a Deep Learning Classification model capable of detecting driver behavior from images captured by dashboard cameras in automobiles.
The model indicates whether the driver is:
   1. Driving cautiously and paying attention to the road. 
   2. Using mobile phone.
   3. Distracted by doing other activities like operating the radio, drinking etc.
      
Distracted driving results in numerous collisions, injuries, and fatalities. Our primary objective is to enhance road safety by employing technology to identify drivers who are distracted. To train the model, we provided it with a dataset containing various actions of the driver. After that, we evaluated the application to ensure optimal functionality. If effective, this might help improve road safety and save lives by reducing the occurrence of accidents involving distracted drivers.

Dataset:-

Kaggle, an online platform for data science competitions, offers datasets for cutting-edge algorithmic challenges in sectors less exposed to AI advancements. It provides a platform to understand datasets deeply and offers opportunities like internships and awards for students. We utilize a dataset from a completed State Farm challenge, which includes hundreds of images depicting various actions performed by multiple individuals.

link- https://www.kaggle.com/competitions/state-farm-distracted-driver-detection

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/3c3ebdef-5eb9-4b24-acee-3d7e930864e9)
Images of the dataset classes

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/2476ee82-05aa-4a0c-affc-8a9cf2fddedc)
Number of Images per subject

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/37956160-de95-4db3-8d25-1351774614af)
Distribution of classes

Modules used:-

1. CNN (Base Line) - The Convolutional Neural Network (CNN) baseline model is a fundamental architecture for image processing. It comprises convolutional layers (Conv2D) that extract essential features, such as edges and patterns, from images. MaxPooling layers assist in downsampling and simplifying information, while Fully Connected Layers make decisions based on the extracted features.

2.MobileNet - MobileNet is a lightweight deep learning model designed for mobile and edge devices. It features depth-wise separable convolutions, where standard convolutions are split into depth-wise and point-wise convolutions. This architecture reduces computational complexity while maintaining accuracy, making it suitable for resource-constrained environments.

3.ResNet - Residual Networks (ResNet) are known for introducing residual learning, addressing the vanishing gradient problem in deep neural networks. It utilizes residual blocks, allowing the model to skip connections and learn residual functions. This architecture facilitates the training of very deep networks, promoting better feature extraction and representation.

4.VGG - The Visual Geometry Group (VGG) architecture is characterized by its simplicity and uniform structure. It consists of repeated blocks of convolutional layers with small 3x3 filters, ReLU activations, and max pooling. This straightforward design facilitates understanding and implementation, making it a popular choice for image classification tasks.

Result:-

All models were trained using the Adam optimizer, set at a learning rate of 0.001. We employed Sparse Categorial Cross entropy as our loss function, couple with a SoftMax activation function in the final output layer. The use of ‘Sparse” was dictated by our class representation, which was numeric rather than one-hot encoded.
![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/b78329ff-7228-4ef5-9b1a-a794ae37cccd)

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/398bd2d4-4b11-497e-8d3e-f58334aff579)
Baseline results- First shows training and validation loss per epoch and second shows training and validation accuracy.  

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/594dd136-a0a0-40b9-b937-4b96b5ee76d4)

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/6edde5fe-7922-4614-a516-5ced3351d3aa)
MobileNet’s results- First one shows traing and validation loss per epoch, and second shows training and validation accuracy.

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/532a5966-e3b4-41d8-a89d-929d1426accc)

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/adb46f0a-e12f-4762-8ad1-0f73fa437552)
VGG results- First shows training and validation loss per epoch and second shows training and validation accuracy.

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/8aca1516-459c-419b-82ea-0504245b6da4)

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/ad6bc0ce-5d82-4054-838b-e1d7fe8dc303)
ResNet results- First shows training and validation loss per epoch and second shows training and validation accuracy.  

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/b1bced40-7ece-492c-b9dc-0bfb53501417)

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/7b443af6-0776-491e-9276-2a571756e8c2)
Every model’s result plotted together- First shows test loss per epoch, and second shows test accuracy.

These Figures present the training and validation losses and accuracies for our Baseline, MobileNet, VGG and ResNet models, respectively, with Figure 8 providing a comparative overview. Notably, ResNet, MobileNet, and VGG training were halted early due to stagnation over four epochs, while our baseline model continued for an additional 10 epochs. This extended training period is attributed to the baseline’s larger parameter space allowing for incremental improvements.

The results demonstrated the feasibility of achieving over 95% accuracy in both training and testing. VGG emerged as the most effective model, marginally outperforming the baseline model, followed by MobileNet and ResNet. VGG’s depth, even with fixed CNN features, provided sufficient high-level information for complex decision-making. Our baseline model, though less parameterized that VGG was specially trained for this task, resulting in high accuracy. MobileNet, while less accurate, offered a significant computational speed advantage, which could be crucial in real-time applications prioritizing frame rate over accuracy.


















