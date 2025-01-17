## Team: Mistletoe <img align="right" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTNrFsIu_0BIWuO5Bji5Vg6Cfm1_AeuIrH83A&usqp=CAU">

## Member: 
Tianjie Zhang(tjzhang@u.boisestate.edu), 

Amanda Jo Mullins, 

Steven Kim, 

Yang Lu

## Abstract:

We mainly used Generative adversarial network(GAN) to augment images in this competition. In the whole competing process, we try to perform some image-preprocess such as **Histogram equalization**, and some **filters** including Median, Gamma, Gaussian etc. However, all the image preprocess methods showed an accruacy decrease in the final result. Also, we tried to use the **traditional image augmentation methods** like crop, noise, flip. These methods did not improve the final result. We were successful on utilizing **Generative adversarial network** to produce fake road images. It produced a variety of different images depending on our training data. Thankfully, we got good results which proves that it is a powerful method to augment the preexisting pavement images. Our final accuracy is around 0.633.


## How to run:
1. Create the environment with conda env create: 
```python 
conda env create -f environment.yml 
```
You can also update an environment to make sure it meets the current requirements in a file:
```python 
conda env update -f environment.yml
```
2. Annotate the second batch of training Data released from [DSPS](https://github.com/UM-Titan/DSPS) using [CVAT](https://github.com/openvinotoolkit/cvat). Put the images and annotation file into the **td4** folder under **cvat** folder.
- This is the my team's [annotation file](https://drive.google.com/drive/folders/1jkkRo5sqSx3fx6E3wf5B0C3mBXeU2CoM?usp=sharing) for the second batch of training data.
3. Run the GAN.ipynb (Generative adversarial network) code to produce some fake road images. 
- To reproduce what we have done, download all the necessary libraries (make sure you have done the step.1), and change the value of **dataset = ""** to your desirable location. 
- Training is performed through the images in the **ng** folder, and validating is performed through the images in the **ok** folder under the **dataset** directory. 
- We suggest to change the parameters **n_epochs, n_cpu, img_size, sample_interval** according to your system's specification and the time you have, but we highly suggest you to keep the rest of the parameters.

4. We choose the best 100 fake images to train, then annotate these images also using [CVAT](https://github.com/openvinotoolkit/cvat). Put the images and annotation file into the **td5** folder under **cvat** folder.

- This is the link for the [fake road images](https://drive.google.com/drive/folders/1Rg_UjVoAPVt8mSX_NLXREd9ETduR9W1L?usp=sharing) we choose from the all produced images.  
- This is the [annotation file](https://drive.google.com/drive/folders/1_Mnn-SUaA6edrmm8pFcqjPFKBI91u8iY?usp=sharing) for the 100 fake images. 

5. Run the dsps_main.ipynb (the Yolo model provided by the [DSPS](https://github.com/UM-Titan/DSPS))

## links

News: https://www.boisestate.edu/computing/2022/05/10/bsu-student-team-places-2nd-in-fhwa-student-data-competition/

Paper: https://arxiv.org/pdf/2206.04874.pdf
