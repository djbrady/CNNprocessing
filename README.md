# CNNprocessing

Image capture and estimation consists of several challenges with easily modeled forward processes but challenging inverse problems. Such challenges include:

- demosaicking from color filter sampling
- creating all infocus images from focal stacks
- creating hdr images
- stitching images 

Since these processes involve images that are at least coarsely registered, CNN processing is likely be ideal for image estimation. Processing may include physical preprocessing for registration, flow compensation, warping etc, followed by some network stack for synthetic image generation. 

Here we are interested in generating training data for such processes. In general, it may be difficult to acquire well constructed and registered training data. We propose that it will be better to generate synthetic training data with known objects. This repository contains notebooks that explore the generation of such training data. 

The underlying concept is that image components are invariant under a variety of transformations, such as rotation, cross range and longitudinal translation, scaling, focal bluring, illumination scaling. We can use such transformations on just a few "eigen features" to create rich data sets for training set generation. 
