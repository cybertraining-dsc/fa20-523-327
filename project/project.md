# Trending Youtube Videos Analysis

[![Check Report](https://github.com/cybertraining-dsc/fa20-523-327/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-327/actions)
[![Status](https://github.com/cybertraining-dsc/fa20-523-327/workflows/Status/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-327/actions)
Status: in progress


* Adam Chai, fa20-523-327
* [Edit](https://github.com/cybertraining-dsc/fa20-523-327/blob/main/project/project.md)

{{% pageinfo %}}

## Abstract

In this modern era of the internet revolution, consumption of all media types is easier than ever. Going onto the internet and finding interesting content takes less than minute to do. In the already growing industry of amateur video production, Youtube is the go to platform for viewers and creators to collide. However, it is harder for video creators to make an interesting video most people can enjoy than a viewer to find one of those videos. This report will address this issue by creating a prediction of how Youtube popularizes a video and a solution to make a video go viral.

Contents

{{< table_of_contents >}}

{{% /pageinfo %}}

**Keywords:** youtube, videos, trending, popular


## 1. Introduction

The final project for this class will be focused on trending Youtube videos. Specifically, this project will be using a trending Youtube videos dataset (US only), and will be used to predict if a video will trend on Youtube. Trending videos on Youtube are aimed to surface videos to a wide range of audience whom find interesting. There are a lot of hypothesis people created to understand the Youtube algorithm, and the Google Staff has hinted what will make a video trend,

Are appealing to a wide range of viewers

Are not misleading, cickbaity, or sensational

Capture the breadth of what's happening on YouTube and in the world

Showcase a diversity of creators 

Ideally, are suprising or novel

but these criterians Youtube has set are not defined[1]. Meaning, the determinants for how a Youtube video will trend will not be given out and it is up for Youtube content creators to find this out themselves. Youtube content creators are constantly attempting to crack this code, evolving and purposely tailoring their videos in hopes it will go viral. Creating Youtube videos that can appeal to a wide audience is difficult. Most people on Youtube have specific interests and follow certain industries, however; anyone can appreciate a good video.

## 2. Background Research and Previous Work

After reviewing other background literature and works from other authors witin this field, most people have not really ventured into how a video will trend on Youtube. Most findings online are analysis or unique findings of popular videos. Several people have done research to predict if a video will be popular on Youtube but do not cover the scope if it will reach the trending section on Youtube. These findings can still be helpful and lead this research into the right direction, however; the analysis done for this project will mostly be new.

## 3. Choice of Data-sets

To understand what determines if a video will trend on Youtube the datasets chosen for this project are a trending Youtube videos (US) and a dataset of public Youtube videos[2][3]. 

The model being built for this project will be using Decision Tree and Random Forest. Decision Tree can be used as a multi-classifier with tree-like structure, since there are unlimited number of layers, decision tree can achieve a high accuracy and cause an overfitting problem. Random Forest will randomnly select samples and features to train different trees and averages the score of different trees therefore reducing overfitting [4].

Afterwards, the model is built wihtin the trending dataset it will be applied onto the data set of public Youtube videos and will be evaluate how accurate the model is at predicting a trending Youtube video. To test if this works the datasets can be compared to find which video trended and if the dataset was able to predict the trending videos on the public videos dataset then it will be successful. 

## 4. Methodology

### 4.1. Hardware Component

This section will be addressed once I go to office hours

### 4.2 Software Component

This section will be addressed once I go to office hours

## 5. Inference

This section will be addressed upon completion

## 6. Conclusion

This section will be addressed upon completion

## 7. Acknowledgments 

Adam Chai would like to thank Dr. Gregor Von Laszewski, Dr. Geoffrey Fox, and the associate instructors in the *FA20-BL-ENGR-E534-11530: Big Data Applications* course (offered in the Fall 2020 semester at Indiana University, Bloomington) for their continued assistance and suggestions with regard to exploring this idea and also for their aid with preparing the various drafts of this article.

## 8. References

[^1]: Google Staff, Trending on Youtube, Google. <https://support.google.com/youtube/answer/7239739?hl=en#:~:text=Trending%20helps%20viewers%20see%20what's,surprising%2C%20like%20a%20viral%20video.>

[^2]: Jolly. Mitchell, Trending YouTube Video Statistics, Kaggle. <https://www.kaggle.com/datasnaek/youtube-new>

[^3]: Jain, Guarav, Youtube Scrapped Data, Kaggle. <https://www.kaggle.com/gaurav2022/youtube-scrapped-data>

[^4]: Li. Yuping, Eng. Kent, Zhang. Liqian, YouTube Videos Prediction: Will this video be popular?, Stanford <http://cs229.stanford.edu/proj2019aut/data/assignment_308832_raw/26647615.pdf>

[^5] Chai, Adam <https://github.com/cybertraining-dsc/fa20-523-327/blob/main/project/youtubeanalysis.ipynb>

[^cloudmesh-benchmark]: Gregor von Laszewski, Cloudmesh StopWatch and Benchmark from the Cloudmesh Common Library, <https://github.com/cloudmesh/cloudmesh-common>

