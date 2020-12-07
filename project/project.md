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

* Are appealing to a wide range of viewers

* Are not misleading, cickbaity, or sensational

* Capture the breadth of what's happening on YouTube and in the world

* Showcase a diversity of creators 

* Ideally, are suprising or novel

but these criterians Youtube has set are not defined[1]. Meaning, the determinants for how a Youtube video will trend will not be given out and it is up for Youtube content creators to find this out themselves. Youtube content creators are constantly attempting to crack this code, evolving and purposely tailoring their videos in hopes it will go viral. Creating Youtube videos that can appeal to a wide audience is difficult. Most people on Youtube have specific interests and follow certain industries, however; anyone can appreciate a good video.

## 2. Background Research and Previous Work

After reviewing other background literature and works from other authors witin this field,  people have ventured into how a video will be popular on Youtube. Most findings online are analysis or unique findings for popular videos. Several people have done research to predict if a video will be popular on Youtube but do not cover the scope if it will reach the trending section on Youtube. These findings can still be helpful and lead this research into the right direction.

## 3. Choice of Data-set

To understand what determines if a video will trend on Youtube the dataset chosen for this project is a trending Youtube videos dataset (US)[2]. 

The Trending Youtube dataset contains 40,949 entries and 16 labels covering the basic information of a trending Youtube video. 

| Label      | Description |
| ----------- | ----------- |
| video_id| unique video id|
| trending_date| the date when a video trended on Youtube|
| title| title of the video|
| channel_title| name of channel that created the video|
| category_id| category of video|
| publish_time| time and date when the video was uploaded|
| tags| kewords associated with the video|
| views| the amount of views a video has    |
| likes| the amount of likes a video has|
| comment_count| the amount of comments commented|
| thumbnail_link| link to thumbnail|
| comments_disabled| boolean variable for allowing comments|
| ratings_disabled| boolean variable for allowing ratings (likes, dislikes)|
| video_error_or_removed| boolean variable if a video is still available|
| description| the description of the video|

The dataset was retrieved from the popular data science website, Kaggle, and many people have done analysis on it. These labels will be used in creating a model to discover how a video will trend on Youtube. The drawbacks of using this dataset are various labels are not covered such as the number of subscribers a channel has or the likelihood of someone that sees the video will click on it and older data is being used (all videos were uploaded and trended between 2017 and 2018).

## 4.Data Preprocessing 

All work done on this project was completed through Google Colab. Once the dataset is imported from Kaggle onto Google Colab data preprocessing is necessary to translate the raw data into a readable format. Pandas and Datetime are used for data preprocessing. 

To begin there are several labels which can be taken out of the model as they do not appear revelant or cannot be run through the model:

* video_id: unique identifier for each video not necessary to use
* title: cannot be translated into a numerical value
* channel_title: cannot be translated into a numerical value
* tags: many tags appear irrelevant to the actual video therefore this will be taken out
* thumbnail_link: cannot be ran through model
* description: irrelevant, does not add value to most videos 

To address duplicates within the dataset after checking all records there are no duplicates within the dataset, except for descriptions which are empty. After removing descriptions from the dataset duplicates will no longer be an issue. 

Several labels need to be converted into an integer so they can be ran through the model:

* trending_date

* publish_time

* comments_disabled

* ratings_disabled

* video_error_or_removed

Python reads the trending_date and publish_time labels as objects which needs to be changed to integer values. To convert the data type the labels first need to be converted into datetime. After, another datetime function will be used to convert the month, day, and year into their own columns. 

![Figure 1](https://user-images.githubusercontent.com/66979171/101300290-f6a75080-37e9-11eb-9e7c-61b067cae41f.png)

Next the remaining three labels can be easily converted from their boolean values into 1/0 values.

![Figure 2](https://user-images.githubusercontent.com/66979171/101300375-3ec67300-37ea-11eb-8197-faa05a5d0565.png)

## 5. Model

The model being built for this project will be using Decision Tree and Random Forest. Decision Tree can be used as a multiple regression with tree-like structure, since there are unlimited number of layers, decision tree can achieve a high accuracy and cause an overfitting problem. Random Forest will randomnly select samples and features to train different trees and averages the score of different trees therefore reducing overfitting [4].

To begin model creation the 80/20, Train/Test Ratio, will be used to create the model. In computing, the Pareto Principle is a safe and common approach for model creation[6]. To determine the accuracy of the model an explained variance score will be applied to determine accuracy. Explained variance is the measure of discrpenecy between a model and actual data [7]. The best possible score is 1.0 meaning there is a stronger strength of association. When creating the model it is important to check if there are highly correlated predictors in the model or else the possibility of multicollinearity can occur. To find highly correlated variables Pearon's correlation coefficient can be used. Correlation coefficients are used to measure how strong a relationship is between two variables [8]. A value of one indicates a strong positive relationship whereas negative one indicates strong negative realtionship. 

![Figure 3](https://user-images.githubusercontent.com/66979171/101300399-5271d980-37ea-11eb-8f48-efabc9d7e0d0.png)



## 6. Conclusion

This section will be addressed upon completion

## 7. Acknowledgments 

Adam Chai would like to thank Dr. Gregor Von Laszewski, Dr. Geoffrey Fox, and the associate instructors in the *FA20-BL-ENGR-E534-11530: Big Data Applications* course (offered in the Fall 2020 semester at Indiana University, Bloomington) for their continued assistance and suggestions with regard to exploring this idea and also for their aid with preparing the various drafts of this article.

## 8. References

[^1]: Google Staff, Trending on Youtube, Google. <https://support.google.com/youtube/answer/7239739?hl=en#:~:text=Trending%20helps%20viewers%20see%20what's,surprising%2C%20like%20a%20viral%20video.>

[^2]: Jolly. Mitchell, Trending YouTube Video Statistics, Kaggle. <https://www.kaggle.com/datasnaek/youtube-new>

[^3]: Jain, Guarav, Youtube Scrapped Data, Kaggle. <https://www.kaggle.com/gaurav2022/youtube-scrapped-data>

[^4]: Li. Yuping, Eng. Kent, Zhang. Liqian, YouTube Videos Prediction: Will this video be popular?, Stanford <http://cs229.stanford.edu/proj2019aut/data/assignment_308832_raw/26647615.pdf>

[^5]: Chai, Adam <https://github.com/cybertraining-dsc/fa20-523-327/blob/main/project/youtubeanalysis.ipynb>

[^6]: Pradeep, Gulipalli.  The Pareto Principle for Data Scientist, KDnuggets. <https://www.kdnuggets.com/2019/03/pareto-principle-data-scientists.html>

[^7]: Statistics How Staff, Explained Variance Variation, StatisticsHowTo. <https://www.statisticshowto.com/explained-variance-variation/>

[^8]: Statsitcs How Staff, Correlation Coefficient Formula, StatsticsHowTo. <https://www.statisticshowto.com/probability-and-statistics/correlation-coefficient-formula/>

[^cloudmesh-benchmark]: Gregor von Laszewski, Cloudmesh StopWatch and Benchmark from the Cloudmesh Common Library, <https://github.com/cloudmesh/cloudmesh-common>

