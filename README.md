# Oxford Pets 

## Objective:

In this project we tried to classify dog and cat images according to their breeds. We used the dataset from the Oxford Pets Kaggle competition, which consists of 7,349 training images and comprises 37 breeds of cats or dogs, which means that we have an average of less than 200 training images per cat or dog breed.

## Result:

 Our model ended up being able to, given the original images, label them like this: 
 
 ![descarga](https://user-images.githubusercontent.com/70718425/104301888-70f18180-54c8-11eb-9613-4f748065a9bf.png)

Our model achieved a testing accuracy of approximately 0.947, with the equal probability benchmark accuracy being 0.027.
After checking that the model's performance was good, I retrained it in all the data, and I used it to participate in the Kaggle competition from which I took the dataset, achieving a multiclass loss of 0.27231, a better performance metric that the one achieved by the winner of the competition:

![score](https://user-images.githubusercontent.com/70718425/104302219-d6457280-54c8-11eb-8def-30a676c9f9d4.png)

With the performance metric being multiclass loss:

![multiclass_loss](https://user-images.githubusercontent.com/70718425/104302308-e6f5e880-54c8-11eb-9698-417223499f9e.png)

## Main technologies used:

* Tensorflow
* Keras
* Matplotlib
* OpenCV
* ImageNet

## Main techniques used:

* Deep Learning
* Modern Computer Vision
* Transfer Learning
* Fine-Tuning 
* Data Augmentation
* Ensemble Learning

## Model:

The final model was an ensemble of ResNet50, ResNet50V2, Xception, Inception, NASNetLarge and InceptionResNetV2, all of them pretrained on the ImageNet dataset, with a new head of units and some regularization.


