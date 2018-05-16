### **Description:** VGG-16 Transfer Learning on Fruits-360 Dataset


* Step-1: Download dataset from [https://www.kaggle.com/moltean/fruits/data](https://www.kaggle.com/moltean/fruits/data). Since I had limited computational resources at hand and wanted to check the results so I used limited number of classes. 
* Step-2: Set the Input Image size to be of shape (100, 100), epochs=5 and batch size as 32.
* Step-3: Use 'glob' to store the input and validation images in respective variables. Also store the files inside training folder to use later to determine number of classes.
* Step-4: Load pretrained weights of VGG-16 on Imagenet and remove the fully connected layers. Freeze the layers while training. Add a dense layer with nodes equal to number of classes followed by activation. 
* Step-5: Create a ImageDataGenerator instance. This is used for Image Preprocessing and Data Augmentation. Use the flow_from_directory function of the instance created earlier to augment the data from the speecified directory
* Step-6: Run the fit_generator to run train_generator and valid_generator i.e run a specific batch and repeat till number of steps.
* Step-7: Create function confusion_matrix even though Scikit-learn provides one. This is done because we need to calculate the target and prediction values.
* Step-8: Plot the training and validation losses and accuracy and confusion matrix.


# Conclusion

* The Algorithm gives a training accuracy of 100% and validation accuracy of 100%. The confusion matrix makes it clear with non-zero entry only in leading diagonal.  
* With no hand engineering the features and minimal hyperparameter tuning the algorithm seems to give excellent results. This suggests how good transfer learning is and can be used as it has state of the art features extracted from training on Imagenet dataset(millions of images).


(NOTE: Only included few classes due to limited computational resources available.)
