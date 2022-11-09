# Fight Detection from Still Images in the Wild
Detecting fights from still images is an important task required to limit the distribution of social media images with fight content, in order to prevent the negative effects of such violent media items. For this reason, in this study we addressed the problem of fight detection from still images collected from web and social media. We explored how well one can detect fights from just a single still image. 

In this context, a new image dataset on the fight recognition from still images task is collected named Social Media Fight Images (SMFI) dataset. The dataset samples gathered from social media (Twitter and Google) and NTU-CCTV Fights <sup id="a1">[1](#f1)</sup> dataset. Since the main concern is recognizing fight actions in the wild, real-world scenarios are included in the dataset where a mass amount of them are spontaneous recordings of fight actions. Using different keywords while crawling the data, the regional diversity is also maintained since the social media uploadings are mostly regional where users share the content in their own language. Some example images from the dataset are given below:

![samples](https://github.com/sayibet/SMFI/blob/main/samples.png)

Both fight and non-fight samples are collected from the same domain where the non-fight samples are also content likely to be shared on social media. Hard non-fight samples are also included in the dataset which displays the actions that might be misinterpreted as fight such as hugging, throwing ball, dancing and more. This prevents the dataset bias, so that the trained models focuses on the actions and the performers on the scene instead of benefiting other characteristics such as motion blur. The distribution of the dataset samples among each class and source is given below:

|           | Twitter | Google  | NTU CCTV-Fights | Total |
|:--------- | :-----: | :-----: | :-------------: | :---: |
| Fight     |  2247   | 162     | 330             | 2739  |
| Non-fight |  2642   | 146     | 164             | 2952 |
| Total     |  4889   | 308     | 494             | 5691  |

Due to the copyright issues the dataset images are not shared directly and the links to the images / videos are shared. As the dataset samples might be deleted in time by the users or the authorities, the size of the dataset is subject to change. 

# Dataset
Please fill out [this form](https://forms.gle/nMWpLbHa9ybhWHAd9) and then email/notify smfi_dataset@googlegroups.com to request the data.

The dataset samples will be shared through a CSV file where the columns are as follows:
- Image ID: Unique ID assigned to each image.
- Class: class of the image as fight / nofight
- Source: The source of the images or videos as twitter_img / twitter_video / google / ntu-cctv
- URL: The link for the images / videos.
  - For Twitter and Google data, image and video URLs are shared.
  - For the NTU CCTV-Fights data, the path to the original video is shared.
- Frame number: If the image is extracted from a video, this column indicates the number of frame within the video.
  - For Twitter videos, the frame number is the number of frame (0-9) out of 10 uniformly sampled frames from each video.
  - For NTU CCTV-Fight videos, the frame number is the number of frame (0-N) out of all frames (N) extracted from each video. 

In order to retrieve the dataset, you should first download the NTU CCTV-Fights [here](https://rose1.ntu.edu.sg/dataset/cctvFights/).

# Citation
Ş. Aktı, F. Ofli, M. Imran and H. K. Ekenel, "Fight detection from still images in the wild", IEEE Winter Conference on Applications of Computer Vision Workshops (WACVW), 2022. 

Paper is available on arXiv: [https://arxiv.org/abs/2111.08370](https://arxiv.org/abs/2111.08370)


### References 

<b id="f1">1</b> Mauricio Perez, Alex C. Kot, Anderson Rocha, “Detection of Real-world Fights in Surveillance Videos”, in IEEE International Conference on Acoustics, Speech, and Signal Processing (ICASSP), 2019 [↩](#a1)
