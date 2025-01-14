[JKUAT_SES_image_classification.pptx](https://github.com/JKUATSES/2021-image-classification/files/7223054/JKUAT_SES_image_classification.pptx)
# 2021-image-classification
Repository to learn image classification
## Introduction - A brief on Image Classification
Image classification is pattern recognition in image data using algorithms. Two methods maybe used:
* Deep learning - uses convolution neural networks to progressively extract higher- and higher-level representations of the image content
  The CNN comprises a stack of modules, each of which performs three operations.
  1. Convolution -extracts tiles of the input feature map, and applies filters to them to compute new features, producing an output feature map, or convolved feature (which may have   a different size and depth than the input feature map). Convolutions are defined by two parameters:
      *Size of the tiles that are extracted (typically 3x3 or 5x5 pixels).
      *The depth of the output feature map, which corresponds to the number of filters that are applied.
  2. Rectified Linear Unit (ReLU)- the CNN applies a  transformation to the convolved feature following each convolution operation, in order to introduce nonlinearity into the model
  3. Pooling - the CNN downsamples the convolved feature (to save on processing time), reducing the number of dimensions of the feature map, while still preserving the most critical feature information. A common algorithm used for this process is called max pooling.
* Transfer learning using pre-trained models
In this image classification both methods were used comparitively and transfer learning had way better performance.
## Technologies and frameworks used
* Languages - Python was used to develop this project
* Platform - Google Colab
* Libraries
  * Pandas
  * Numpy
  * Matplotlib
  * OpenCV, PIL, skimage, matplotlib
* Deep learning frameworks
  * Tensorflow 
  * Keras
* Pre-trained model - MobileNet, weights from ImageNet
## Dataset 
The data used for this project was obtained from a [Zindi challenge](https://zindi.africa/competitions/runmila-ai-institute-minohealth-ai-labs-tuberculosis-classification-via-x-rays-challenge/data). The data have been split into a test and training set. The training set, on which you will train your models, contains 353 images of x-rays of TB-positive lungs and 365 images of x-rays of healthy lungs. The test set contains 82 images.
### Disclaimer

This challenge is solely for educational purposes. Chest X-Rays is one of various tools that can be used for triaging and screening for Tuberculosis. Furthermore, it is possible for an individual to develop different types of infections. This is to be treated purely as an exercise in tool development.

### Acknowledgements

Montgomery County X-ray Set: X-ray images in this data set have been acquired from the tuberculosis control program of the Department of Health and Human Services of Montgomery County, MD, USA.

Shenzhen Hospital X-ray Set: X-ray images in this data set have been collected by Shenzhen No.3 Hospital in Shenzhen, Guangdong province, China. The x-rays were acquired as part of the routine care at Shenzhen Hospital.

It is requested that publications resulting from the use of this data attribute the source (National Library of Medicine, National Institutes of Health, Bethesda, MD, USA and Shenzhen No.3 People’s Hospital, Guangdong Medical College, Shenzhen, China) and cite the following publications:

* Jaeger S, Karargyris A, Candemir S, Folio L, Siegelman J, Callaghan F, Xue Z, Palaniappan K, Singh RK, Antani S, Thoma G, Wang YX, Lu PX, McDonald CJ. Automatic tuberculosis screening using chest radiographs. IEEE Trans Med Imaging. 2014 Feb;33(2):233-45. doi: 10.1109/TMI.2013.2284099. PMID: 24108713
* Candemir S, Jaeger S, Palaniappan K, Musco JP, Singh RK, Xue Z, Karargyris A, Antani S, Thoma G, McDonald CJ. Lung segmentation in chest radiographs using anatomical atlases with nonrigid registration. IEEE Trans Med Imaging. 2014 Feb;33(2):577-90. doi: 10.1109/TMI.2013.2290491. PMID: 24239990
# Contents
## EDA 
Methods used to explore the data include
1. Calaculating contrast pixel values for images 
2. Calculating averages pixel values for images
3. Calculating variability 
4. Calculating standard deviation 
5. Getting Eigen Images 
6. Getting the diiferences between the two classes the pixel values for images in the two classes
## Visualizations
Histogram Plots were used to visualize image data 
## Preprocessing 
Preprocessing techniques include 
* Contrast enhancement through
    * Histogram equaliation


     ![image](https://user-images.githubusercontent.com/58877986/134502836-2f388e77-26f2-4dd5-9245-bef88866a718.png)
    * CLAHE
    
     ![image](https://user-images.githubusercontent.com/58877986/134502709-4a817987-5da3-4c62-8a91-7824b0cf8d4e.png)
     ![image](https://user-images.githubusercontent.com/58877986/134508220-314d477e-da73-4449-a984-86d624668aa1.png)
    * Data Augmentation 
    
     ![image](https://user-images.githubusercontent.com/58877986/134505411-b3c3922e-46ba-43b7-bd5f-3d1c3b8f2e79.png)

## Building the model 
The first model used contained 2 layers, and was a CNN built from scratch
The second model used transfer learning 

# REFERENCES
* https://medium.com/analytics-vidhya/image-equalization-contrast-enhancing-in-python-82600d3b371c
* https://www.mygreatlearning.com/blog/introduction-to-image-pre-processing/
* https://jannik-zuern.medium.com/using-a-tpu-in-google-colab-54257328d7da
* https://towardsdatascience.com/image-enhancement-techniques-using-opencv-and-python-9191d5c30d45
* https://machinelearningmastery.com/how-to-control-the-speed-and-stability-of-training-neural-networks-with-gradient-descent-batch-size/
* https://developers.google.com/machine-learning/practica/image-classification/convolutional-neural-networks
* https://www.kdnuggets.com/2019/08/introduction-image-segmentation-k-means-clustering.html
* https://machinelearningmastery.com/how-to-improve-performance-with-transfer-learning-for-deep-learning-neural-networks/
* https://towardsdatascience.com/how-to-choose-the-best-keras-pre-trained-model-for-image-classification-b850ca4428d4
* https://towardsdatascience.com/hacking-your-image-recognition-model-909ad4176247
* https://towardsdatascience.com/exploratory-data-analysis-ideas-for-image-classification-d3fc6bbfb2d2
* https://medium.com/analytics-vidhya/opencv-findcontours-detailed-guide-692ee19eeb18
* https://docs.opencv.org/master/d7/d4d/tutorial_py_thresholding.html

