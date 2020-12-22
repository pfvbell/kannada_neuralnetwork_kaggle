# kannada_neuralnetwork_kaggle

# **Project 2: Kannada MNIST Kaggle submission**
[Full Github](/images/kannada_neuralnetwork_kaggle)

This entry was placed 252 in the kaggle competition with a final test accuracy of 91.8%. Validation Accuracy was 95.8% and train accuracy was 99.7%.
Images of kannada digits were classified as '0' or '1' using a regularised feed-forward neural network (including L2 and dropout). 2000 epochs were used, with a batch size of 32.

![](/images/one.png) ![](/images/zero.png)

I took a sequential approach, changing one hyperparameter at a time and seeing if changing that hyperparameter improved the model. If it did improve the model then I kept the change and tried a different adaptation. However, I took a logical order through the various hyperparameter options. I started by adjusting Adam. I realised that you must start with small numbers (coefficients) for L2 regulaization and increase them. Small numbers mean less penalisation in this instance. However, using too high values for the coefficients resulted in the penalisation reducing the ability for the model to train on the data and therefore resulted in lower scores. Therefore I used a value in between these extremes. My validation score is much higher than the test score on kaggle which may suggest that there is a lot of noise in the data and the model is fitting to that noise. Therefore, data augmentation would be useful in this instance.

Below is the accuracy (left) and loss (right).
![](/images/Accuracy%20and%20Loss.png)

## Data
The Kannada MNIST dataset was used, which is a large database of handwritten digits in the indigenous language Kannada.

This dataset consists of 60,000 28x28 grayscale images of the ten digits, along with a test set of 10,000 images.

For this homework, we will simplify the problem by only using the digits labeled 0 and 1 owing to the similarity of the two symbols, and we will use a total of 1,200 samples for training (this includes the data you will use for validation).

More details: https://arxiv.org/pdf/1908.01242.pdf
