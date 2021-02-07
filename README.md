# Oxford Pets: Project Overview

* Created a model that could classify dog and cat images according to their breeds, participating in a Kaggle Competition.

## Steps:

* Downloaded the images from Kaggle.
* Implemented and trained AlexNet from scratch on the train split.
* Used Transfer Learning for better results on different models.
* Created an ensemble of the best models.
* Participated in the Kaggle Competition, achieving a better result than the winner.

 ## Main technologies used:

* Tensorflow
* Keras
* Matplotlib
* OpenCV
* ImageNet
* Pandas

## Main techniques used:

* Deep Learning
* Modern Computer Vision
* Transfer Learning
* Fine-Tuning 
* Data Augmentation
* Ensemble Learning

## Visualizing the data:

I used the Oxford Pets Kaggle dataset, which consists of 7,349 training images and comprises 37 breeds of cats or dogs, which means that it has an average of 200 training images per cat or dog breed.

Let's see some of the images along with their labels:

![descarga (4)](https://user-images.githubusercontent.com/70718425/107144586-69dd5800-693c-11eb-8012-fff76387742f.png)

## Training AlexNet from scratch:

I built the architecture and trained it on the train split, achieving a validation accuracy of 0.366. I did this to compare the results with transfer learning.

## Using Transfer Learning:

I imported some networks pretrained on the ImageNet dataset, replaced their fully connected layers and retrained them. These were the results:

|  Model | Validation Accuracy  | 
|---|---| 
|  Equal Probability Benchmark |  0.027 |
| ResNet50  |  0.889 |
| ResNet50V2  | 0.899  |
|  Xception |  0.924|
|  Inception |  0.927 |
|  NASNetLarge |  0.937 |
|  InceptionResNetV2 |  0.942 |

## Ensemble Modelling:

I created an ensemble of the networks using a weighted average of the predictions. **It had a test accuracy of 0.947.** 
Let's see the ensemble predict the labels from some images of the test set:
![descarga](https://user-images.githubusercontent.com/70718425/104301888-70f18180-54c8-11eb-9613-4f748065a9bf.png)

## Kaggle Competition Results:

After checking that the ensemble's performance was good, I retrained the models on all the data and used the ensemble to participate in the Kaggle Competition, achieving a multiclass loss of 0.27231, a better performance metric that the one achieved by the winner of the competition:

![score](https://user-images.githubusercontent.com/70718425/104302219-d6457280-54c8-11eb-8def-30a676c9f9d4.png)

With the performance metric being multiclass loss:

![multiclass_loss](https://user-images.githubusercontent.com/70718425/104302308-e6f5e880-54c8-11eb-9698-417223499f9e.png)
