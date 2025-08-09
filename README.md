# DS-Final-Project-NeuroLearn
Deep learning image recognition model that analyzes MRI scans to detect/classify brain conditions using learned image features. 

# Project Scope
Focus on one type of brain condition to build a targeted model for. Focus will look at building a model to identify when an image is a brain glioma in a Basic Color Map dataset versus another brain condition. The images will include both brain glioma and other types of brain conditions (specifically brain meningioma). 

Brain glioma refers to a type of tumor that originates in the glial cells of the brain, which provide support and protection to neurons. Gliomas are often aggressive and can occur in various parts of the brain, leading to symptoms like headaches, seizures, and cognitive impairments.

# Dataset
## Brain Cancer MRI Colorized Dataset
- https://www.kaggle.com/datasets/shuvokumarbasakbd/brain-cancer-mri-colorized-dataset/data 
- focus: Brain Glioma - Basic Color Map (2004 files)

## Basic Color Map
Applies a standard color palette (like Jet or Viridis) to grayscale data. Different intensities are mapped to different colors, enhancing the visual discrimination of anatomical or pathological regions in the image.


### Citation (Raw Data Source):
Rahman, Md Mizanur (2024), “Brain Cancer - MRI dataset”, Mendeley Data, V1, doi: 10.17632/mk56jw9rns.1
https://data.mendeley.com/datasets/mk56jw9rns/1

# Model Development 
- Normalized image pixel values and compelte train/test('validation') split in preparation for deep learning image recognition model use
- Developed model architecture - build Convolutional Neural Network (CNN) model using TensorFlow Keras. Specifically, using tf.keras.Sequential which is a standar API in TensorFlow for building deep learning image recognition models. CNN is suited for image classification tasks and is a classic deep learning architecture for image recognition.
- Compiled the model - specify the optimzer, loss, and metrics
- Trained the model - fit model using model.fit()
- Evaluted and visualized - evaluate the performance of the model on test data


# Model Performance and Final Summary 
## Summary Model Outputs
Overall Performance 
- Training Accuracy: 85.33%
- Test Accuracy: 85.87%

Indicates a consistent performance between training and testing, suggesting low overfitting.

## Classification Report Summary 
Two classes were evaluated:
- Glioma - Basic_Color_Map
- Meningioma - Basic_Color_Map

- Metric	    Glioma	Meningioma
- Precision	0.86	0.86
- Recall	    0.86	0.86
- F1-Score	0.86	0.86
- Support	    400	    400

Macro Average: 0.86 across all metrics (treats all classes equally).

Weighted Average: 0.86 (accounts for class imbalance, which seems minimal here).

This indicates balanced model performance across both tumor types.

## Confusion Matrix Interpretation
Correct predictions:
- 343 Glioma correctly classified
- 344 Meningioma correctly classified

Misclassifications:
- 57 Gliomas incorrectly predicted as Meningiomas
- 56 Meningiomas incorrectly predicted as Gliomas

The confusion matrix is very symmetric, meaning the model is equally likely to misclassify either class.

## Key Takeaways
- Model achieves solid performance (≈86%) in classifying two brain tumor types from images.
- Balanced precision, recall, and F1-score indicate no class bias.
- Low misclassification rate, and no sign of overfitting.
- Could be improved with data augmentation, hyperparameter tuning, or more complex architectures if needed.




