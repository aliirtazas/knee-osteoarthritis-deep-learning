# Knee Osteoarthritis Prediction Using Deep Learning 

**Predicting severity of Knee Osteoarthritis using SOTA deep learning**

### Overview 

The project aims to develop an automated system for classifying the severity of knee osteoarthritis 
(OA) using X-ray images. We employ advanced deep learning models (VGG19 and Xception) with 
transfer learning and customized weights to achieve a 5-class classification scheme.  To prepare the 
images for optimal model performance, implemented custom image processing techniques. 

### Data

The data was collected from two unique sources. The training data comprises 9786 datapoints 
distributed across three classes. This training data is split into five classes with noticeable class 
imbalance.  

![f2f27164-adae-4dda-a067-ec935c3001b4](https://github.com/user-attachments/assets/aebb44df-b3a1-4b31-b20f-38fe8dcbef1d)


For validation and testing, 7828 datapoints are used, with 65% 
allocated for validation and 35% for testing.

![83498312-7e9a-4b9d-a634-88eaea3ee818](https://github.com/user-attachments/assets/140b9013-ff68-4c80-a928-764473a8c876)

### Data Pre-processing

The images were preprocessed in several steps to prepare them for analysis.  First, they were resized 
to a consistent dimension and converted to grayscale for simplified processing.  Pixel values were 
then normalized to standardize brightness and contrast across the dataset.  To reduce noise, Gaussian 
blurring was applied, followed by histogram equalization to enhance the visibility of important 
features. This preprocessing methodology likely aims to optimize the images for use in a machine 
learning model.

### Model Comparison and Performance Summary

This project explores multi-class image classification using VGG19 and Xception, comparing their performance with and without additional convolutional layers.

**Baseline VGG19 Model**
The pre-trained VGG19 base model without additional convolution layers achieved an accuracy of 49%, indicating suboptimal performance. While Class 0 had the highest recall (90%), other classes, especially Class 1, performed poorly (0% recall). The overall precision and F1-score remained low, suggesting the need for further fine-tuning and feature extraction improvements.

**VGG19 with Additional Convolution Layers**
After modifying the VGG19 architecture by adding custom convolutional layers, the model's performance significantly improved, achieving 92% accuracy. Precision and recall increased across all classes, with Class 4 achieving 100% in both metrics. The enhanced model demonstrated better generalization and more balanced classification, making it a strong candidate for the task.

**Xception Model**
The Xception model, known for its depthwise separable convolutions, achieved 91% accuracy, performing slightly below the modified VGG19. While it excelled in recall (96% macro avg), indicating better sensitivity to true positives, it had lower precision in some classes (e.g., Class 4: 77% precision). The model demonstrated strong performance but slightly less balanced predictions compared to VGG19.

### Conclusion

Both modified VGG19 and Xception models performed significantly better than the VGG19 base model. While VGG19 achieved the highest accuracy (92%) with balanced precision and recall, Xception provided higher recall (96%), making it better at identifying true positives. The choice between models depends on the application:

Use VGG19 if balanced accuracy and precision are priorities.
Use Xception if recall and sensitivity to positive cases are crucial.
