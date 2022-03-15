# Movement_analysis

<a name="table_of_contents"/>

## Table of Contents
1. [Instructions](#instructions_)
2. [Introduction](#introduction_)
3. [Development](#development_) 
4. [Conclusion](#conclusion_)
5. [License](#license_)

<a name="instructions_"/>

## Instructions

As we have programmed it is mandatory to create a directory named "resultats" on your computer. This directory has to be located in the same directory where your MATLAB program is. In this directory you will find all the differents pictures generated by our MATLAB program.

You need to download the "seq1" directory from this repository and to put it in the same directory where the MATLAB program is. In the seq1 directory you will find all the images from the security camera.

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/Image1.png?raw=true)

_Figure 1: Photograph to indicate the placement of the resultats and the seq1 directories._


[Table of Contents](#table_of_contents)
<a name="introduction_"/>

## Introduction

The aim of this program was to analyse the datas (pictures) of a security camera in order to detect the objects in movement.

[Table of Contents](#table_of_contents)
<a name="development_"/>

## Development

The idea is to analyze the pictures from a sequence in order to detects movements. For that, we have followed several distinct methods which will be explained in this GitHub.

To have an idea of the pictures we have to analyze, here are some of them (01, 10, 20, 30, 40 and 50) :

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/seq1/seq1_01.jpg?raw=true)
![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/seq1/seq1_10.jpg?raw=true)
![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/seq1/seq1_20.jpg?raw=true)
![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/seq1/seq1_30.jpg?raw=true)
![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/seq1/seq1_40.jpg?raw=true)
![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/seq1/seq1_50.jpg?raw=true)

_Figure 2: Photographs extracted from the sequence of pictures we had._

Here is our image of interest (the picture number 13) on which the analysis will be based : 

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/resultats/11_image_num_13.jpg?raw=true)

_Figure 3: Photograph of interest._

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/resultats/12_image_num_13-5.jpg?raw=true)

_Figure 4: Photograph of the image number 8._

Then we have made the difference between the image number 13 and the image number 8 in order to see the vehicles which have moved between the two.

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/resultats/13_diff_image___delta_i_5.jpg?raw=true)

_Figure 5: Photograph of the image difference (image 13 - image 8)._

By thresholded the image difference, we want to highlight the objects in movement between the 2 images.

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/resultats/14_th_diff_image___delta_i_5___k_th_4.0.jpg?raw=true)

_Figure 6: Photograph of the image difference (image 13 - image 8) thresholded._

Then, we do the average of all the images of the sequence.

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/resultats/101_Image_of_averages.jpg?raw=true)

_Figure 7: Photograph of the image average._

Then, we save the image of standard deviations.

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/resultats/102_Image_of_standard_deviations.jpg?raw=true)

_Figure 8: Photograph of the image of the standard deviations._

On the two past photographs, we can observe all the trajectories.

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/resultats/113_abs_diff_image___delta_i_5.jpg?raw=true)

_Figure 9: Photograph of the image (in absolute value)._

From figure 9, we are able to obtain the three next figures :

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/resultats/122_th_diff_image_minus_median___k_th_4.0.jpg?raw=true)

_Figure 10: Photograph of the image minus median (thresholded)._

We only obtain the pixels where there is movement. We use the median image because it allows us to have less noise.

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/resultats/212_Ferm_Ouv_th_diff_image_minus_median___k_th_4.0.jpg?raw=true)

_Figure 11: Photograph of the image minus median (thresholded) with Closing and then Opening._

By doing a Closing then Opening we are able to dilate white elements on a picture.

![alt text](https://github.com/Clerbout-Francois/Movement_analysis/blob/main/resultats/214_RCC8_Ferm_Ouv_th_diff_image_minus_median___k_th_4.0.jpg?raw=true)

_Figure 12: Photograph of the image minus median (thresholded) with Closing and then Opening and a 8-connexity._

[Table of Contents](#table_of_contents)
<a name="conclusion_"/>

## Conclusion

We liked this project because it corresponded to our expectations in terms of work to be done and it also allowed us to progress in the field of computer vision. 

Indeed, we spent several hours on this project and chose to work in the following way : one of us coded and the other was there to proofread the code (and vice versa), this allowed us to progress much faster as we limited the errors of inattention. Of course it was not always the same person who coded and the same for the person in charge of proofreading.

Furthermore, we are aware that we could continue to develop this program in order to complete and improve it. The next step will be to develop an AI.

[Table of Contents](#table_of_contents)
<a name="license_"/>

## License
Project carried out with Maël Lemaire. You can see his GitHub [here](https://github.com/lemaireMael).

Please do not forget that this project is under [MIT license](https://choosealicense.com/licenses/mit/).



[Table of Contents](#table_of_contents)
