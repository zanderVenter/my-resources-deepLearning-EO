# my-resources-deepLearning-EO
Gathering all the resources I used in learning deep learning for earth observation. I have focussed on Pytorch implementations.

## Other useful catalogues of deep learning resources
- [satellite-image-deep-learning](https://github.com/satellite-image-deep-learning) - annotation, datasets, model-training-and-deployment, software, techniques all related to deep learning applied to satellite and aerial imagery.
- [Awesome Remote Sensing Change Detection](https://github.com/wenhwu/awesome-remote-sensing-change-detection) - List of datasets, codes, and contests related to remote sensing change detection.
- [Awesome_Satellite_Benchmark_Datasets](https://github.com/Seyed-Ali-Ahmadi/Awesome_Satellite_Benchmark_Datasets) - To the best of our knowledge, and to the best of our findings, until May 2021, the following graph displays more than 90% of the benchmark datasets in remote sensing and photogrammetry.
- [torchrs](https://github.com/isaaccorley/torchrs) - PyTorch implementation of popular datasets and models in remote sensing
- [torchgeo datasets](https://github.com/microsoft/torchgeo/tree/main/torchgeo/datasets) - benchmark and other datasets that have been integrated into torchgeo

## Courses and tutorials I have completed
- [Udemy course: PyTorch for Deep Learning and Computer Vision](https://www.udemy.com/course/pytorch-for-deep-learning-and-computer-vision/?couponCode=LEADERSALE24A)
- [Youtube videos from 3Blue1Brown](https://www.youtube.com/@3blue1brown)
- [Mauricio Cordeiro's end-to-end Pytorch tutorial](https://www.geocorner.net/post/artificial-intelligence-for-geospatial-analysis-with-pytorch-s-torchgeo-part-1)
    - Ran through original
    - Adjusted to include U-Net with ResNet34 backbone instead of the default ResNet50. I used [segmentation_models_pytorch](https://github.com/qubvel/segmentation_models.pytorch) after recommendation from Geethen.
    - Adjusted to make inference on new images
    - Adjusted to cater for multi-class land cover segmentation
        - Played around with image patch sizes
        - visualizing predictions alongside validation labels
        - exploring over-fitting by plotting training and validation loss
        - tried pre-trained weights for encoder initialization - from ImageNet (didn't really help - made more blobby)
        - try different architecture like DeepLabV3+ (coded for in original tutorial, but without smp) instead of U-Net to help resolve smaller landscape features (didn't really help - made more blobby)
        - (todo) try data augmentation
        - (todo) extract class-wise probability scores
        - (todo) Geethen suggested trying [FeatUp](https://github.com/mhamilton723/FeatUp) to try address the blobbiness issue

## Next steps for me
- [Do this Pytorch course](https://www.learnpytorch.io/)
- [Test out foundational EO models like prithvi using terratorch](https://ibm.github.io/terratorch/?)
- [test out some segmentation_models_pytorch examples](https://segmentation-modelspytorch.readthedocs.io/en/latest/)
- [try out DynamicEarthNet change detection](https://github.com/aysim/dynnet)
- [try replicate this Landsat-based TempCNN and Transformer for change detection](https://github.com/Patawaitte/FoDiM/tree/main)

## Code snippets and helpers I have used so far and plan to use
- [Earth_Engine_training_patches_computePixels.ipynb](https://github.com/google/earthengine-community/blob/master/guides/linked/Earth_Engine_training_patches_computePixels.ipynb)
- [Glenn Moncrieff's TempCNN](https://github.com/GMoncrieff/renosterveld-monitor/blob/main/02_model_fit.ipynb) - although this is in TensorFlow it may still be useful
