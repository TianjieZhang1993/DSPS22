## Team: Mistletoe <img align="right" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTNrFsIu_0BIWuO5Bji5Vg6Cfm1_AeuIrH83A&usqp=CAU">

## Member: Amanda Jo Mullins, Steven Kim, TJ Zhang(tjzhang@u.boisestate.edu), Yang Lu

We mainly use Generative adversarial network(GAN) to augment images in this competition. In the whole competiting process, we try to do some image-preprocess like **Histogram equalization**, some **filters** including Median, Gamma, Gaussian ... However, all the image preprocess methods showed an accruacy decrease in the final result. Also, we try to use the **traditional image augmentation methods** like crop, noise, flip ..., but these still did not improve the final result. Eventually, we made a try in using the **Generative adversarial network** to produce fake road images. It could make totally different images depending on our training data. Thankfully, it shows that it is a powerful way to augment the pavement images which we already have. We got an accuracy around 0.633.


## Procedure:
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

