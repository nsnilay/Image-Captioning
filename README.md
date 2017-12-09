# Image-Captioning
Final year Project based Internship project inspired by Andrej Karpathy's CS231n

## Datasets used
  Flickr8k
  Flickr30k
  MSCOCO
  
Libraries needed - 
Tensorflow, keras, python 3.xx, nnumpy

You will need to download InceptionV3 weights and our model weights beforehand and store them in their respective folders, details of which are given in Description file of the respective directories.


## Summary and Conclusions

Our project involved collecting, pre-processing, training and inference the data. We used different datasets of different sizes. We tried on different models like we first used LSTM in place of GRU. We experimented with various hyper-parameters like learning rate and batch size. When we started getting decent results we continued with the model and hyper-parameters to train the model for larger epochs. Finally we were able to build a webapp that could generate captions to any given image. We tried deploying the webapp on Internet but due to limited availability of computational power and money, we were unable to do so.

Initially when the model was trained less and with LSTM, it used to predict the colour wrong. Sometimes there was only one man in the caption while there were many in the picture. Also using normal argmax prediction, the model used to get stuck in the loop. After using Beam prediction the problem was resolved. By using GRU and training it for more epochs, the model started predicting more accurate captions. Since the dataset has many images of dogs in it, our model works very well on images of dog but at the end it began generating good captions even with humans in it.

Our model gives state of the art captions to any new image outside of the training data. Our final model is trained only on Flick8k dataset. With the availability of more computation power, we believe that our model can outperform several of the related models as our model is able to generate accurate captions without much need of data pre-processing.
We have used Bidirectional GRU which no one has used for Image Captioning as far as we know. 

There is a lot of scope for future work in Image Captioning. It is always difficult to generalize the model. If we have a lot of animal pictures in our dataset, our model might be biased to dogs and will perform poorly if there are humans in the image. Thus a huge amount of datasets are involved for the better model. Huge datasets implies faster computation and larger memory. This makes it difficult to carry out the research in the field. One can come up with efficient models but it requires a lot of time and resources to test the models.


