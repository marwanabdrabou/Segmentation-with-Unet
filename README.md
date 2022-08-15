# Table of contents
* [General info](#general-info)
* [Input Pipeline](#input-pipeline)
* [About U-Net](#about-u-net)
* [Model Architecture](#model-architecture)

## General info
The objective of this project is to identify the range of nuclei in biomedical images in order to automate the process of identifying the nuclei.It will improve the efficiency of drug testing and shorten the time for a new drug launch in the market.Since the nuclei had various of shape and size.Therefore, the semantic segmentation would be the best approach for this project.

## Input Pipeline
Dataset contain test and train folder, it consist of 67 images and masks and 603 images and masks respectively(train-test with a ratio of 90:10).The input shape of each image were reshaped and modified the channel to 128x128 with RGB channel.While the masks images were converted to the grayscale image.Apart from that, all the label of the masks preprocessed to values of 1 or 0.Besides, the images pixel value was preprocessed into range of [0,1].Next,data augmentation was implemented where the images and masks were flipped horizontally.

## About U-Net
In this article, we explore U-Net, by Olaf Ronneberger, Philipp Fischer, and Thomas Brox. This paper is published in 2015 MICCAI and has over 9000 citations in Nov 2019. U-Net is used in many image segmentation task for biomedical images, although it also works for segmentation of natural images. U-Net has outperformed prior best method by Ciresan et al., which won the ISBI 2012 EM (electron microscopy images) Segmentation Challenge.[More](https://towardsdatascience.com/biomedical-image-segmentation-u-net-a787741837fa)

## Model Architecture
![U-net](https://user-images.githubusercontent.com/73760366/184727133-a5fa22a9-b6c5-4b0b-8888-deb3de2acc36.png)


|             | Training | Validation |
| ----------- | -------- | ---------- |
| Loss        | 0.0869   | 0.0913     |
| Accuracy(%) | 96.65    | 96.65      |

![output](https://user-images.githubusercontent.com/73760366/184732243-b7be1582-e1d8-42ad-9725-de4323436197.jpg)
![loss](https://user-images.githubusercontent.com/73760366/184732255-4c248e83-606b-4f81-b374-26b9b186b444.jpg)
