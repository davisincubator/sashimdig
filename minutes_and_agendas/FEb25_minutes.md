# Minutes for February 25, 2017

### Status Updates:
* Jared
    * Found a how-to for running things on the GPU, will try it Monday the 27th
    * Found some papers on picking layers for the CNN, will skim them and let us know which are good
* Abbie
	* Successfully padded images and ran the model on the padded images
	* Successfully gray-scaled images, but didn't run the model on them due to needed to adjust code further (fewer channels)
	* Did not luminance or color balance images, because there wasn't as easy a function for this
	* Going forward it seems like luminance and color balancing might be a really good way to reduce noise, so she will focus on this rather than grayscaling
* Danielle
	* Made her first jupyter notebook, yay!
	* Will focus on fish versus no-fish going forward, since it is necessary for our bounding box plan
* Jason
	* Got up and running with tensorboard, and it is very pretty
	* He also found some code on stack overflow to display the convolutions
	* He also found a good website from Karpathy for visualizing the steps of the CNN
	
###Abbie's Tensorboard notes
* Tensorboard is party of tensorflow, so we all already have it
* When you run your model you can use the "tensorboard_verbose = n" notation to save your training information
* n can be set to 0, 1, 2, or 3 depending on how much information you want it to save
* n = 0 for log-loss and accuracy
* Tensorboard will automatically make pretty visualization regarding your model

### We discussed:
* We seem to have plateaued at log-loss = 1.6
* This is likely because our images are very noisy and have a lot of nuisance information, like the boat, water, people
* Perhaps we could reduce this noise by cropping to the fish, luminance, and color balancing
* We also may want to use pre-trained NNs, since they seem better

### We want to:
* luminance and color balance (currently Abbie)
* identify the binary fish versus no-fish (currently Danielle)
* crop to fish, possibly with [this code](https://www.kaggle.com/c/the-nature-conservancy-fisheries-monitoring/discussion/29131) (currently no one)
* use a pre-trained model (currently no one)
* Possibly run on GPU (Jared) or AWS (Jason) as complexity increases this may become more important

### Jason's resources:
* [CS231n ConvNet Demo](https://cs.stanford.edu/people/karpathy/convnetjs/demo/cifar10.html)
