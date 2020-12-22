# kannada_neuralnetwork_kaggle

# **Project 2: Kannada MNIST Kaggle submission**
[Full Github](/images/kannada_neuralnetwork_kaggle)

This entry was placed 252 in the kaggle competition with a final test accuracy of 91.8%. Validation Accuracy was 95.8% and train accuracy was 99.7%.
Images of kannada digits were classified as '0' or '1' using a regularised feed-forward neural network (including L2 and dropout). 2000 epochs were used, with a batch size of 32.

![](/images/one.png) ![](/images/zero.png)

I took a sequential approach, changing one hyperparameter at a time and seeing if changing that hyperparameter improved the model. If it did improve the model then I kept the change and tried a different adaptation. However, I took a logical order through the various hyperparameter options. I started by adjusting Adam. I realised that you must start with small numbers (coefficients) for L2 regulaization and increase them. Small numbers mean less penalisation in this instance. However, using too high values for the coefficients resulted in the penalisation reducing the ability for the model to train on the data and therefore resulted in lower scores. Therefore I used a value in between these extremes. My validation score is much higher than the test score on kaggle which may suggest that there is a lot of noise in the data and the model is fitting to that noise. Therefore, data augmentation would be useful in this instance.

Below is the accuracy (left) and loss (right).
![](/images/Accuracy%20and%20Loss.png)
