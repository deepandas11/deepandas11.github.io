---
layout: post
title:  "Incremental Learning"
categories: deep-learning, computer-vision, detection, incremental-learning
--- 


## A Catastrophe

Imagine training an object detection model on an extensive amount of data, with well-defined label and bounding box annotations. State of the art detectors perform quite well and clever tweaks like the Focal Loss mechanism have led to the development of single-stage detectors with comparable or even better accuracy. However, even with the most extensive of datasets, a problem still persists, and is quite **catastrophic** in nature.

The problem is called *catastrophic forgetting* and stems from the fact that the model trained on the given dataset is able to classify amongst a finite set of objects. When new classes are added, one might be tempted to train the existing model on these samples and expect the model to not only correctly detect objects of the new category, but also objects from the older category. However, the model's performance when it comes to the older classes, diminishes dramatically. A workaround this problem is to train the model on the entire collection of data, both old and new. The troubles associated with this approach is quite evident. Even if this can be done for one or two new classes, it becomes unsustainable for incrementally growing number of classes. Put simply, traditional Deep Learning models need to have all the data available to them while training. They are not equipped to selectively learn about new data with a small collection of the data. 

The Paper discussed here is titled ["End-to-End Incremental Learning"](https://arxiv.org/abs/1807.09536) and discusses an approach to learn deep neural networks incrementally, using new data and only a small exemplar set corresponding to samples from the old classes. The end-to-end learning objective comprises of two parts: A distillation based measure to retain knowledge from old classes, and a usual cross entropy based measure to learn new classes. The approach discussed here is Incremental as, it has the ability to train itself from a flow of data and performs decently well, while classifying both old and new classes. It is also an end to end system where the classifier and feature representation is updated in a joint fashion. Essentially, this method can be plugged into any deep learning architecture by replacing the traditional loss function with a cross distilled loss function.

## Distillation - It's a thing

Before we move ahead to discuss more about the cross-distilled loss, we might as well discuss a bit about the Distillation technique proposed here in this paper titled ["Distilling the Knowledge in a Neural Network"](https://arxiv.org/abs/1503.02531). Now, this paper is really interesting in its own right, and no surprised there, having been written jointly by Hinton, Vinyals and Jeff Dean. The entire objective of the paper is to present an approach where one can train a highly complex model on a large amount of data and empower the model to extract structure from the data. Following this training, the authors have shown a way to transfer this knowledge to a small model that is more suitable for deployment and has less rigid requirements in terms of latency or performance.

When an image is passed to an Image Classification network, we identify the knowledge learnt in the model by checking the log probability of the correct answer. For instance in the figure below, the model is able to classify the image correctly, as the probability is highest for the category **Husky**. However, the question at hand is: *How do we change the form of the model but keep the same knowledge?*. By training the model on the objective of maximizing ground truth log probability, a beneficiary side effect that we can observe is that the model assigns probabilities to all incorrect answers as well. Even though these probabilities are really small, some of them are much larger than the others. For instance, the categories *Wolf* and *Dog* have much higher probability than say, *Washing Machine*. Quoting from the paper itself:
> These  relative probabilities of incorrect answers tell us a lot about how the cumbersome model tends to generalize. 

<img src="{{site.url}}/images/increm_1.png" style="display: block; margin: auto;" />

