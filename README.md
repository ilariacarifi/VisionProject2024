# VisionProject2024
PROJECT TOPIC: GENERATIVE MODEL (GANs)

TASK: Realistic images generation/Image Super-Resolution

ID student: 1696976 1999362

PROJECT TOPIC: GANs

GAN is about generating data starting from another type of data or from noise. It is composed by a discriminative network and a generative network. Those models are able to produce some images even if starting from random noise.
GANs (Generative Adversarial Networks) are machine learning models made by a combination of two neural networks: generator (decoder part) and discriminator (critic part), which compete with each other to become more accurate in their predictions:
-	The generator goal is to artificially manufacture outputs that could easily be mistaken for real data.
-	The discriminator goal instead is to identify which outputs that it receives have been artificially created.
In order to accomplish both tasks, GANs use adversarial training. For instance, if we use a dataset made by images, the generator creates “fake” images and tries to fool the discriminator in believing that the images are real, while the discriminator tries to discriminate as good as possible real images from the ones created by the generator.
TASK
One application of use could be about calcifications recognition in Mammography using Data Augmentation.
Calcifications are breast changes related to the presence of a pathology which, depending on the case, can be benign or malignant. These lesions are the result of the deposition of calcium salts in the breast tissue and, due to their marked contrast to X-rays, can be visualized by mammography, which is a X-ray picture of the breast.
The calcifications are visible almost exclusively on mammography. The distinction between benign malignant calcifications is made according to their characteristics on mammography examination.
We would implement a GAN model which is able either to:
-	Generate increased resolution images of mammography (Image Super-Resolution task), in order to recognize on those medical images, if there are calcifications and even their characteristics, possibly without adding noise. Indeed, poor image quality reduces the accuracy of deep learning medical image models.

To accomplish this task, we need to find pairs of low/high resolution images.

-	Generate realistic images (Data Augmentation task), in order to increase the size of the dataset. The performance of medical image recognition models highly depends on the representativeness and sufficiency of training samples. However, the amount of data available for training models able to predict the correct diagnosis through mammography examination is very limited. This leads to possibilities of model overfitting (due to insufficient data or imbalanced data categories). A possible way to deal with this issue is to perform synthetic data generation of medical images based on the existing training data. We would like to use a GAN in order to synthesize medical images, in particular for medical image calcification recognition

By GANs, the reconstruct of approximate real data could be as follows:
-	The generator produces synthetic images
-	The discriminator is trained to detect the synthetic images from real images, validating in this way the effectiveness of the generative network
The generated synthetic images are used then to train a classification model (CNN for instance) or a segmentation model for calcification recognition

Our final choice about one of the two tasks depends on if we will be able to find enough or appropriate images samples (or even a pre-build dataset). 
The dataset that we would use for the project is this one http://peipa.essex.ac.uk/pix/mias/, but we are considering to increase the size of this one (even by adding by hand more samples) or to find other sample images on the web.
