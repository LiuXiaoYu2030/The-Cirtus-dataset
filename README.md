# The-Citrus-dataset
## Overview
In this study, our ultimate goal was to develop an object detection algorithm for applications such as fruit thinning and harvesting. An Intel RealSense D455 depth camera was used for image acquisition, which has been widely used in these applications. The shooting distance was between 0.5 m and 2 m. 

Fruit images were collected from three experimental orchards of the Guangxi Academy of Specialty Crops, China. These orchards are located in Lingui City (110◦7 032.300 N,25◦7 034.500 E), Guilin, China. The permission for sample collection was granted by the Guangxi Academy of Specialty Crops. In this experiment, four citrus varieties, “Kumquat”, “Nanfeng tangerine”, “Fertile tangerine”, and “Shatang tangerine” were selected. Images were collected starting in spring when the diameter of the fruit was approximately 5 cm,until autumn in 2020 when the fruit was mature. Images were taken twice a week and four times in a day at 9:00 am, 11:00 am, 2:00 pm, and 4:00 pm, respectively. Finally, 500 images were collected from “Kumquat”, 400 images from “Nanfeng tangerine”, 300 images from “Fertile tangerine”, and 300 images from “Shatang tangerine”. The RGB images of the four varieties of citrus are shown in Figure 1.

![fig1](/images/fig1.png)


## Dataset annotation and augmentation
LabelImg was used as the image annotation tool. When using LabelImg to mark the citrus fruits, the position and classification of the citrus fruits was marked. During the labeling process, dense and occluded fruits were also labeled separately.

Data augmentation on the original dataset can increase the diversity and robustness of the experimental dataset. The Imgaug image data augmentation library was used to augment the citrus datasets. Considering the actual interference factors of the natural environment, several processes were used in the augmentation including rotating the original image, adjusting the image color, and adding noise. By performing the augmentation described above, a dataset containing 16,000 images was created and used to train and test the YOLOv5 model.The local effects after image enhancement are shown in Figure 2.

![fig2](/images/fig2.png)

## Downloads
The citrus dataset and annotations are about 3.82GB in size and can be downloaded through Baidu Cloud:

    Link: https://pan.baidu.com/s/1IQbsvJTlxEd4QXcZm0q2EA  
    password：vpoi

## License
The dataset is available to download for commercial/research purposes under a Creative Commons Attribution-ShareAlike 4.0 International License. The copyright remains with the original owners of the images.


## Citation
    @article{liu2022detection,
      title={Detection of dense Citrus fruits by combining coordinated attention and cross-scale connection with weighted feature fusion},
      author={Liu, Xiaoyu and Li, Guo and Chen, Wenkang and Liu, Binghao and Chen, Ming and Lu, Shenglian},
      journal={Applied Sciences},
      volume={12},
      number={13},
      pages={6600},
      year={2022},
      publisher={MDPI}
    }

