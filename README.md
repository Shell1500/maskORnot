# maskORnot
## An image classifier that detects weather an image contains a person wearing a mask or not.


##### Built using [pytorch](https://pytorch.org/) and [fastai](https://www.fast.ai/).
##### Using [this](https://www.kaggle.com/omkargurav/face-mask-dataset) dataset.

## Requirements
Google Colab and a Google Drive account.

## Usage
To train the model yourself run the `train.ipynb` on Google Colab using a GPU runtime.
To test the model run the `test.ipynb` on Google Colab. (No web app as of yet).

## Description

The program uses an openly available kaggle dataset with over 7500 images of individuals with and without facemasks.
The fast AI library is used to train a pre-trained [Convolutional neural network](https://en.wikipedia.org/wiki/Convolutional_neural_network) called [ResNet](https://pytorch.org/hub/pytorch_vision_resnet/)

## Training Process

- After the dataset was downloaded, the images were fed into a data-loader for their sizes to be changed and labels be added.
![test_dataset](https://user-images.githubusercontent.com/40688468/118412609-5d436b00-b6b4-11eb-9013-c75e39925230.png)

- After which the data was fed into the network (resnet18 - 18 Layers) and trained on the Google Colab GPU.
![training](https://user-images.githubusercontent.com/40688468/118412650-9d0a5280-b6b4-11eb-983f-44d2e7c047b9.png)


- Very Low loss values and Confusion Martrix Consistent.

![confusion_matrix](https://user-images.githubusercontent.com/40688468/118412735-15711380-b6b5-11eb-8ec8-672f41fdf4d8.png)

- Images that were ambiguous or invalid were the most confusing to the model as expected.

![unsure](https://user-images.githubusercontent.com/40688468/118412811-7bf63180-b6b5-11eb-8871-8e7f9356b14b.png)


## Testing

- Testing the trained model using an image in the drive. Shows Very High confidence.
![test](https://user-images.githubusercontent.com/40688468/118412842-a6e08580-b6b5-11eb-8520-b4db7b2a4e66.png)


