# Image_classifier
Image classifier based on Inception model.

These instructions mainly introduce how to retrain the whole Inception's model for new categories.

These instructions are mainly based on tensorflow's built-in scripts and functions, and a few modifications of the script may be added. In fact the tutorials of how to use them can be accessed in Tensorflow's official website or Github. However when I tried to use them, I find some of the links and scripts given are broken or out of dated. So These instructions are written to just collect and summarize useful information from Tensorflow. 

Inception is Google's CNN model for classifying images, which has been fine trained for 1000 classes in ImageNet dataset. 
Here assuming we have some other datasets, for example, 11 kinds of fruits and vegetables images which consist of totally around 14,000 images. And we want to make this Inception_v3 model applicable in our case. One idea is to just tune this model's output layer's parameters. The reason our final layer retraining can work on new classes is that it turns out the kind of information needed to distinguish between all the 1,000 classes in ImageNet is often also useful to distinguish between new kinds of objects.

However, another more complicated idea is to retrain the whole network thoroughly, which may get a better result on our customized categories.

The steps about how to implement the two ideas mentioned above will be introduced.
