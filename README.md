## Team name: Mistletoe <img align="right" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTNrFsIu_0BIWuO5Bji5Vg6Cfm1_AeuIrH83A&usqp=CAU">

## Team member: Amanda Jo Mullins, Steven Kim, TJ Zhang, Yang Lu

## procedure:
1. Annotate the second batch of training Data released from DSPS. Put the images and annotation file into the 'td4' folder in 'cvat' folder.
- This is the annotation file for the second batch of training data. https://drive.google.com/drive/folders/1jkkRo5sqSx3fx6E3wf5B0C3mBXeU2CoM?usp=sharing
2. Run the GAN(Generative adversarial network) code to produce some fake images. choose the best 100 images then add into the training dataset.
- To reproduce what we have done, download all the necessary libraries, and change the value of **dataset = ""** to your desirable location. Training is performed through the images in the **ng** folder, and validating is performed through the images in the **ok** folder under the **dataset** directory. We suggest to change the parameters **n_epochs, n_cpu, img_size, sample_interval** according to your system's specification and the time you have, but we highly suggest you to keep the rest of the parameters.
- This is the link for the fake images we choose from the all produced images.  https://drive.google.com/drive/folders/1Rg_UjVoAPVt8mSX_NLXREd9ETduR9W1L?usp=sharing
- This is the annotation for the 100 fake images. https://drive.google.com/drive/folders/1_Mnn-SUaA6edrmm8pFcqjPFKBI91u8iY?usp=sharing



## code

