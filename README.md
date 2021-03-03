# DL_COVID-19_Face_mask_detection
Introduction

The COVID-19 pandemic continues to have a devastating effect on the health and well-being of the global population. A critical step in the fight against COVID-19 is effective screening of infected patients, with one of the key screening approaches being radiology examination using chest radiography. It was found in early studies that patients present abnormalities in chest radiography images that are characteristic of those infected with COVID-19[21]. Motivated by this and inspired by the work done by researchers so far, in this study we have designed a deep convolutional neural network design tailored for the detection of COVID-19 cases from chest X-ray (CXR) images. The objective behind developing this model is to work towards the development of highly accurate yet practical deep learning solutions for detecting COVID-19 cases thereby accelerating the treatment of those who need it the most.

Methodology

Models deployed:

 MobilNet transfer learning were utilized to address this supervised image classification problem. The MobilNet transfer learning model consisted of approximately 36.9 million parameters out of which approximately 21k were non-trainable parameters. For the exact layout of both the models refer to the model summary in the oral presentation.

Building the model For both the models the following hyperparameters and metrics were employed:

- ‘Adam’ was used as an optimizer with a learning rate of 0.0001
- ‘Sigmoid’ was used as the activation function for the output layer. ReLU was employed as activation functions for the other layers to avoid forwarding of any negative values through the network[35].
- Being a supervised classification problem, the system performance was evaluated mainly by using binary accuracy, and binary cross-entropy [33][34]. Furthermore, precision, recall, and F1-score were also computed for each class (COVID-19, and Normal) to obtain a more realistic result.
- Number of epochs of 500, batch size of 64, and a patience of 5 were used for training the model.
- Three call backs were defined, namely Early Stopping, Monitor, and Learning Rate Scheduler for both the models as discussed below: 
  • Early Stopping was employed to stop the training of the model early if there was no increase in validation set accuracy. 
  • Model Checkpoint was employed to save the model by monitoring validation accuracy. It was set such that it would save the model to disk only if the validation accuracy of the model in current epoch was greater than what it was in the last epoch. 
  • The learning rate scheduler was defined such that after every 10 epochs the learning rate would reduce by a factor of 2.

Results and Discussion

MobilNet transfer learning model

The MolbilNet model outperforms the CNN models by demonstrating an accuracy of 96% and a loss of 0.58 on the test dataset. 
