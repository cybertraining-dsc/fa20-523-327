# Trending Youtube Videos Analysis
* Adam Chai, fa20-523-327
* [Edit](https://github.com/cybertraining-dsc/fa20-523-327/blob/master/project/project.md)

{{% pageinfo %}}

## Abstract

need to add abstract

Contents

{{< table_of_contents >}}

{{% /pageinfo %}}

**Keywords:** youtube, videos, trending


## 1. Introduction

The final project for this class will be focused on trending Youtube videos. Specifically, this project will be using a trending Youtube videos dataset (US only), and will be used to predict if a video will trend on Youtube. Trending videos on Youtube are aimed to surface videos to a wide range of audience whom find interesting. There are a lot of hypothesis people created to understand the Youtube algorithm, and the Google Staff has hinted what will make a video trend,

Are appealing to a wide range of viewers
Are not misleading, cickbaity, or sensational
Capture the breadth of what's happening on YouTube and in the world
Showcase a diversity of creators 
Ideally, are suprising or novel

but these criterians Youtube has set are not defined[1]. Meaning, the determinants for how a Youtube video trends are not clearly defined. Youtube content creators are constantly attempting to crack this code, evolving and purposely tailoring their videos in hopes it will go viral. Creating Youtube videos that can appeal to a wide audience is difficult. Most people on Youtube have specific interests and follow certain industries, however; anyone can appreciate a good video.

## 2. Objective

The objective of this project is to develop a model to predict if a Youtube video will trend. Content creators, companies, or even one time users aim for their videos to reach the trending section on Youtube. When counting the amount of videos that are on the trending section one can easily see there are only 50 videos a day that will reach it. Even if a video is popular it is still incredibly difficult for the video to reach the trending section. As stated earlier, the purpose of the trending section is to attract a wide range of audience but what if there is an easier way for a video to reach the section. For my model to predict if a video will trend I will be training my model on the trending youtube videos and after will be applied to all youtube videos. While training my model I will be constantly evaluating the validity of its findings and the accuracy. If this model is successful it can be used to increase the chances a video will trend on Youtube. 

## 3. Dataset
To understand what determines if a video will trend on Youtube the datasets chosen for this project are a trending Youtube videos (US) and a dataset of public Youtube videos[2][3]. 

The model being built for this project will be using Decision Tree and Random Forest. Decision Tree can be used a multi-classifier with tree-like structure, since there are unlimited number of layers, decision tree can achieve a high accuracy and cause an overfitting problem. Random Forest will randomnly select samples and features to train different trees and averages the score of different trees therefore reducing overfitting [4].

Afterwards, the model is built wihtin the trending dataset it will be applied onto the data set of public Youtube videos and will be evaluate how accurate the model is at predicting a trending Youtube video. To test if this works the datasets can be compared to find which video trended and if the dataset was able to predict the trending videos on the public videos dataset then it will be successful. 

## 4. Work Breakdown
Initial Project Report - completed
Predictive Model - undertermined, need to visit office hours, look into model again

## 5. References
[^1]: Google Staff, Trending on Youtube, Google. <https://support.google.com/youtube/answer/7239739?hl=en#:~:text=Trending%20helps%20viewers%20see%20what's,surprising%2C%20like%20a%20viral%20video.>

[^2]: Jolly. Mitchell, Trending YouTube Video Statistics, Kaggle. <https://www.kaggle.com/datasnaek/youtube-new >

[^3]: Google Research Team, Youtube8m, Research Google. <http://research.google.com/youtube8m/index.html>

[^4]: Li. Yuping, Eng. Kent, Zhang. Liqian, YouTube Videos Prediction: Will this video be popular?, Stanford <http://cs229.stanford.edu/proj2019aut/data/assignment_308832_raw/26647615.pdf>

