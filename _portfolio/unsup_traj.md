---
title: "Unsupervised Anomalous Trajectory Detection for Crowded Scenes"
excerpt: "Published Research Work<br/><img src='/images/unsup_traj.png'>"
collection: portfolio
---


An improved clustering based, unsupervised
anomalous trajectory detection algorithm for crowded
scenes has been shown here. The proposed work is based on four major steps, namely:
* Extraction of trajectories from crowded scene video
* Extraction of several features from these trajectories
* Independent mean-shift clustering
* Anomaly detection.

First, the trajectories of all moving objects in a crowd are extracted using a multi feature video object tracker. These trajectories are then transformed into a set of feature spaces. Mean shift clustering is applied on these feature matrices to obtain distinct clusters, while a Shannon Entropy based anomaly detector identifies corresponding anomalies. In the final step, a voting mechanism identifies the trajectories that exhibit anomalous characteristics. The algorithm is tested on crowd scene videos from datasets. The videos represent various possible crowd scenes with different motion patterns and the method performs well to detect the expected anomalous trajectories from the scene.


The published paper can be [found here](/files/78_DeepanDas.pdf)

The link to the Github Repository can be [found here.](https://github.com/deepandas11/HAN-and-Data-Augmentation-Text-Classifier)