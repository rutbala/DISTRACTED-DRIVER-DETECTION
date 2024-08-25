# DISTRACTED-DRIVER-DETECTION

Introduction:-

In this project, I developed a deep learning classification model leveraging advanced computer vision techniques to detect driver behavior from images captured by dashboard cameras. The model utilizes Convolutional Neural Networks (CNNs) to accurately classify driver actions into categories such as attentive driving, mobile phone usage, and other distractions, including operating the radio or drinking. By training on a comprehensive labeled dataset of driver behaviors, the model effectively identifies distracted driving with high precision. Our objective is to enhance road safety through AI-powered real-time monitoring, aiming to reduce accidents and fatalities by proactively detecting and addressing risky driver behaviors. This AI-driven solution represents a significant step toward improving traffic safety and preventing collisions caused by distracted driving.

Dataset:-

link- https://www.kaggle.com/competitions/state-farm-distracted-driver-detection

Modules used:-

CNN (Baseline): A fundamental deep learning model for image processing, featuring Conv2D layers for feature extraction, MaxPooling for downsampling, and Fully Connected Layers for decision-making.

MobileNet: A lightweight model optimized for mobile and edge devices, using depth-wise separable convolutions to reduce computational complexity while maintaining accuracy, ideal for resource-constrained environments.

ResNet: A deep learning architecture known for residual learning, utilizing residual blocks to address the vanishing gradient problem, enabling the training of very deep networks with enhanced feature extraction.

VGG: A popular image classification model, characterized by its simple and uniform structure, consisting of 3x3 convolutional layers, ReLU activations, and max pooling, offering ease of implementation and effective performance.

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/3c3ebdef-5eb9-4b24-acee-3d7e930864e9)

Images of the dataset classes

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/2476ee82-05aa-4a0c-affc-8a9cf2fddedc)

Number of Images per subject

![image](https://github.com/rutbala/DISTRACTED-DRIVER-DETECTION/assets/165860969/37956160-de95-4db3-8d25-1351774614af)

Distribution of classes

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

These Figures present the training and validation losses and accuracies for our Baseline, MobileNet, VGG and ResNet models, respectively, with the last Figure providing a comparative overview. Notably, ResNet, MobileNet, and VGG training were halted early due to stagnation over four epochs, while our baseline model continued for an additional 10 epochs. This extended training period is attributed to the baseline’s larger parameter space allowing for incremental improvements.

The results demonstrated the feasibility of achieving over 95% accuracy in both training and testing. VGG emerged as the most effective model, marginally outperforming the baseline model, followed by MobileNet and ResNet. VGG’s depth, even with fixed CNN features, provided sufficient high-level information for complex decision-making. Our baseline model, though less parameterized that VGG was specially trained for this task, resulting in high accuracy. MobileNet, while less accurate, offered a significant computational speed advantage, which could be crucial in real-time applications prioritizing frame rate over accuracy.


















