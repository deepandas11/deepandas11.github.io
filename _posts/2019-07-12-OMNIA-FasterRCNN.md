---
layout: post
title:  "Adapting to Cross-Domain Data in Deep Learning: OMNIA Faster R-CNN"
categories: deep-learning, computer-vision, detection
--- 

This is a brief review of the paper titled ["OMNIA Faster R-CNN: Detection in the wild through dataset merging and soft distillation"](https://arxiv.org/abs/1812.02611). This is a fairly recent paper and solves a problem which is quite commonplace with object etectors.


## Introduction 
Widely popular object detectors like Faster R-CNN or SSDs depend on Full Supervision and need instance annotations for each object in each image. What would happen, if say, a new category of objects are introduced in the dataset, or one uses a dataset from another domain to test this trained model's performance? These models are no virtuosos. Quite expectedly, they will perform really bad. This method aims to use several datasets with different categories to increase the number of categories that can be detected. It also uses concepts of transfer learning to enhance domain independence.

One simple approach to this problem would be to train highly specific models for such specific datasets. So, if one needs to detect instances in images pertaining to Fashion elements, one can train a model on very specific images that have instances belonging to categories that need to be detected. If someone needs to detect only cars, train a model on the Cityscape dataset. These models become real experts in their domain but will perform really poorly when tested on the other. We need models that can adapt to domains. In that regard, we would like to benefit from the training done on a more general dataset like MSCOCO and use that knowledge on a dataset like Cityscapes. That helps because it helps reduce false positives. *Being able to detect bottles or fire hydrants improves prediction scores on cars by reducing False Positives.* 

Another approach could be to concatenate the two datasets and train a single model on it. However, the categories in both datasets might have zero or minimal overlap. Let's say Category //C_a// is not present in //Dataset_2// and category //C_b// is not present in //Dataset_1//. In that case upon training a single model on both datasets, all instances of //C_b// will be treated as background in all images of //Dataset_1// and all instances of //C_a// will be treated as background in all images of //Dataset_2//.