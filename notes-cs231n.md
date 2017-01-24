# overview

notes on Stamford CS231n lecture 13

## Segmentation

there are two different subtasks. There are also classic approachs, and 'deep learning' approaches.

### Semantic Segmentation
the semantic segmentation procedure takes an image as input, and, for each
pixel in the image, associates a class label with that pixel.
class labels (building, tree, dog, etc) are fixed in number. Generally, the
collection of class labels included a special 'background' class that
represents objects that don't fit into the other classes.[1](https://youtu.be/UFnO-ADC-k0?t=6m24s)

```haskell
Matrix m n RGB -> Matrix m n Class
```

Note: Instances of classified objects are not differentiated.

### Instance Segmentation

attempts to address 'instance labeling' limitations encountered with 
semantic segmentation.[2](https://youtu.be/UFnO-ADC-k0?t=8m22s)

given an input image, output all instances of the classes contained in
the image, and for each instance segment out the pixels that belong to that
image

#### how does semantic segmentation proceed.

see source [3](https://youtu.be/UFnO-ADC-k0?t=9m25s)

##### Pixelwise

1. extract all patches of input image
2. for each patch, run it through a conv net that classifies the center pixel of the patch

Performing segmentation this way is expensive. In order to avoid this, segmentation can proceed in a 
'fully convolutional' manner. Note: if using this method, downsampling/pooling
will decrease spacial size of output [4](https://youtu.be/UFnO-ADC-k0?t=10m42s)

##### Multiscale Pixelwise
see [5](https://youtu.be/UFnO-ADC-k0?t=12m17s)

## Soft Attention

TODO

# Other Terms Used

* superpixel methods 
* segmentation trees
* iterative refinment
* upsampling
