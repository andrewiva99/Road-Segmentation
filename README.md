# Road segmentation with U-Net

This work is devoted to semantic segmentation of roads using **U-Net**. The **U-Net** architecture is built using  ```torch.nn``` basic modules. We achieved **IoU score** of about **0.8**. 

## Data representation

The training and test data is represented by three-channel images of size **370x370** along with a binary mask. 
The training and test data sizes are **678** and **219**, respectively.

![data_review](https://github.com/andrewiva99/Road-Segmentation/assets/112372506/468008e6-7ad3-4f2f-9660-ea269180b674)

## Training and evaluation
As a loss function, we used a combination of focal loss and dice loss. 
Adam is used as an optimizer with a learning rate of 1e-4 and weight decay of 1e-5. 
Below is the change history losses and IoU score depending on the training epoch.

![history_graph](https://github.com/andrewiva99/Road-Segmentation/assets/112372506/c5c7e37b-3d9a-4cfe-9955-a7cbf429a0be)

## Visualization of segmentation

The line **Predicted** represents the results of the **Image** road segmentation. 
Ground truth segmentation, IoU score and loss are given.

![results_review](https://github.com/andrewiva99/Road-Segmentation/assets/112372506/9f70eac3-d8eb-4460-b264-6750fdc6d721)
