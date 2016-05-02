# dcgan-autoencoder

This implementation slightly adjusts the convolutional autoencoder implementation found here:  https://github.com/mikesj-public/dcgan-autoencoder

The main adjustments are:
* Altering the net input size
* Adding additional convolutional layers to the front of the autoencoder
* Toggling Pooling before MSE
* Adjusting the encoding cost multiplier
* Adding functionality for printing the entire test set
* Adjusting dataprocessing.py to create a masked image dataset

The instructions for running the code are copied below from the original implementation:

## How to run

I assume knowledge of IPython (Jupyter), pip and virtualenv (not complicated to learn if not).  The following should work on unix systems.  Working in a virtualenv, run

```pip install -r /path/to/requirements.txt```

You should download the CelebA dataset from [website](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) (you're looking for a file called img_align_celeba.zip).  Unzip into this directory then run

``` ./dataprocessing.py ```

This will crop the images to the right size and store them in HDF5 format.

Next run the dcgan notbook.
