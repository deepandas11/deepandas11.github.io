---
layout: post
title:  "Adapting to Cross-Domain Data in Deep Learning: OMNIA Faster R-CNN"
categories: deep-learning, computer-vision, detection
--- 

This is a brief review of the paper titled "OMNIA Faster R-CNN: Detection in the wild through dataset merging and soft distillation". This is a fairly recent paper and solves a problem which is quite commonplace with object etectors.


## Introduction 
Widely popular object detectors like Faster R-CNN or SSDs depend on Full Supervision and need instance annotations for each object in each image. What would happen, if say, a new category of objects are introduced in the dataset, or one uses a dataset from another domain to test this trained model's performance? These models are no virtuosos. Quite expectedly, they will perform really bad. This dataset aims to use several datasets with different categories 