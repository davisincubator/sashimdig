# Meeting on February 19, 2017
We discussed:
* We all made pipelines (largely stolen from Jared) and made submissions!
* We are all down-sampling to 90 by 160 now
* But we're surprised our validation accuracy is so much lower than our submission score
Could this be because
* It's overfitting based on something? Image quality? Boat ID?
* The distribution of fish types isn't the same in the training set and test set
We want to in the future:
* Test if it's training on fish by occluding the fish
* Train a model just based on fish versus no-fish (potential problem: there are very few no fish photos
* Remove nuisance features (like the boat) with mean subtraction
* Use a pre-trained CNN
* Try on black and white images (maybe also luminance detected)
* Plot log loss functions and accuracy to help determine learning rate, maybe using tensorflow
* Make sure our validation score is multi-class log loss (because that's what kaggle uses)