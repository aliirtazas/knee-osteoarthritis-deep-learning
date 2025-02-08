# Knee Osteoarthritis Prediction Using Deep Learning 

**Predicting Knee Osteoarthritis using SOTA deep learning**

### Overview 

The project aims to develop an automated system for classifying the severity of knee osteoarthritis 
(OA) using X-ray images. We employ advanced deep learning models (VGG19 and Xception) with 
transfer learning and customized weights to achieve a 5-class classification scheme.  To prepare the 
images for optimal model performance, implemented custom image processing techniques. 

### Data

The data was collected from two unique sources. The training data comprises 9786 datapoints 
distributed across three classes. This training data is split into five classes with noticeable class 
imbalance, as illustrated in Image 1.  For validation and testing, 7828 datapoints are used, with 65% 
allocated for validation and 35% for testing. Image 2 demonstrates the class imbalance present in this 
validation and test data split.

### Data Pre-processing

The images were preprocessed in several steps to prepare them for analysis.  First, they were resized 
to a consistent dimension and converted to grayscale for simplified processing.  Pixel values were 
then normalized to standardize brightness and contrast across the dataset.  To reduce noise, Gaussian 
blurring was applied, followed by histogram equalization to enhance the visibility of important 
features. This preprocessing methodology likely aims to optimize the images for use in a machine 
learning model. 
