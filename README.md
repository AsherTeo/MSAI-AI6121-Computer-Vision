# MSAI-AI6121-Computer-Vision
For Assignment 1, we are given a few images and we are required to use Histogram Equalization (HE) to enhance the performance of the image. However, one of the cons of HE is the overall abnormal brightness in the image. For example, when HE is applied to a dim image, the image may look excessively enhanced especially its brightness. 
Another constrast enhancement method is called Gamma Correction. However, the cons of Gamma Correction is that it is hard to find the correct gamma coefficient for each pixel. Therefore, in this paper [1], the author will be using CDF to find the ideal gamma coefficient. With the help of adaptive gamma correction, it will enhance the constrast of the images especially on dimmed images. 

I have implemented an Enhanced Histogram Equalization algorithm by incorporating the knowledge of previous Histogram Equalization and Adaptive Gamma Correction. [1]

[1] - Gang Cao, Li Hui, HuaWei Tan. Contrast enhancement of brightness-distorted images by improved adaptive gamma correction" 2018


Original:
[sample1](https://user-images.githubusercontent.com/78581569/215753866-f49bb03b-2a43-4c5b-b8bb-74d0f27b2deb.jpg)
[sample5](https://user-images.githubusercontent.com/78581569/215754983-487cfa4c-766b-4966-8365-8ad4a7ca31ac.jpeg)

Histogram Equalization:
[sample1_HE](https://user-images.githubusercontent.com/78581569/215754038-8aa5d7ff-0ae2-400e-92bd-868010c4af13.jpg)
[sample5_HE](https://user-images.githubusercontent.com/78581569/215755279-602d8804-72ca-4db9-86ce-6ad83f360fb8.jpeg)


Enhanced Histogram Equalization:
[sample1_GAMMA](https://user-images.githubusercontent.com/78581569/215754111-c7c2cdc8-ed41-4eb0-9772-dfd324b702d0.jpg)
[sample5 _GAMMA](https://user-images.githubusercontent.com/78581569/215755318-b17242db-8146-4dc0-b5d9-ec2073766711.jpeg)

For Assignment 2, we are given a few pair of images and are required to write a computer algorithm that compute the disparity between left and right of the image. Disparity only can be computed when there are two images lying along the x-axis. The pair of images can create a triangle when facing at the same point. The distance between the two images is called the translation (T) and the distance perpendicular from the object point to the translation is called the depth (Z). I used Sum-of-Squared Difference (SSD) to compute point matching. For more information, please refer to my PDF in Assignment-2. 

![image](https://user-images.githubusercontent.com/78581569/216006020-0c662575-3124-48c7-b2db-6b754d2c2dc7.png) ![image](https://user-images.githubusercontent.com/78581569/216006204-cc1f28c3-62d9-4f90-9a85-5a9e7174f51a.png)


For Assignment 3, I discuss about the existing problems that computer vision is facing and introducing some of the existing Generative Adversarial Net (GAN) such as Pix2pix GAN and CycleGAN to improve the issues. In addition, I also discuss about the correct metrics that we should use for different type of GAN. I trained a model using CycleGAN using red and black dress and the result can be shown below. 

![image](https://user-images.githubusercontent.com/78581569/216008041-ceca5197-ec3c-4f49-96e0-4f7a8f17134d.png)


For the Final Project, we are required to design our own network and train it using MNIST training datasets and evaluate over test datasets. After that, we need to investigate different hyper-parameters such as learning rate, loss function, etc. Lastly, we need to benchmark with the state-of-the-art solutions and discuss the possible improvements. For this project, I trained using two-layers convolutional layers , (1 -> 25) and (25 -> 100), and two linear layers, (4900 -> 100) and (100 -> 10). I experimented different learning rates (0.1, 0.01, 0.001) with different epoches (100, 200). The best result will be further experimented using different optimizers (SGD, Adam and AdamW) and learning rate scheduler (Constant, Cosine Annealing Learning Rate and Step Learning Rate). In neural network, overfitting is a common issue. It normally occurs when the network memorized the training data instead of learning from the training data which lead to poor performance on validation and testing datasets. Therefore, to solve this issue, we need to apply Regularization to Neural Network. The two Regularization methods that I have used are by adding weight decay in the optimizers and applying data augmentation on training datasets such as Horizontal Flip, Random Crop, Cut-out and etc. Finally, I also experimented pre-trained Resnet-18 model. 

Overall Grade: A

