## Team: Mistletoe <img align="right" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTNrFsIu_0BIWuO5Bji5Vg6Cfm1_AeuIrH83A&usqp=CAU">

## Member: Amanda Jo Mullins, Steven Kim, TJ Zhang(tjzhang@u.boisestate.edu), Yang Lu

## Procedure:
1. Create the environment with conda env create: 
```python 
conda env create -f environment.yml 
```
You can also update an environment to make sure it meets the current requirements in a file:
```python 
conda env update -f environment.yml
```
2. Annotate the second batch of training Data released from DSPS. Put the images and annotation file into the 'td4' folder in 'cvat' folder.
- This is the my team's annotation file for the second batch of training data. https://drive.google.com/drive/folders/1jkkRo5sqSx3fx6E3wf5B0C3mBXeU2CoM?usp=sharing
3. Run the GAN.ipynb (Generative adversarial network) code to produce some fake road images. 
4. Choose the best 100 fake images, then annotate these images also. Put the images and annotation file into the 'td5' folder in 'cvat' folder.
- To reproduce what we have done, download all the necessary libraries, and change the value of **dataset = ""** to your desirable location. 
- Training is performed through the images in the **ng** folder, and validating is performed through the images in the **ok** folder under the **dataset** directory. 
- We suggest to change the parameters **n_epochs, n_cpu, img_size, sample_interval** according to your system's specification and the time you have, but we highly suggest you to keep the rest of the parameters.
- This is the link for the fake images we choose from the all produced images.  https://drive.google.com/drive/folders/1Rg_UjVoAPVt8mSX_NLXREd9ETduR9W1L?usp=sharing
- This is the annotation for the 100 fake images. https://drive.google.com/drive/folders/1_Mnn-SUaA6edrmm8pFcqjPFKBI91u8iY?usp=sharing


