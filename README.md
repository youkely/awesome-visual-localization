# Awesome Visual Localization: [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome visual localization resources, inspired by [awesome-computer-vision](https://github.com/jbhuang0604/awesome-computer-vision) and [awesome-visual-localization](https://github.com/siyandong/awesome-visual-localization). Visual localization is the task to estimate the 6 dof pose of an image given a representation of the world created using a set of reference images. The representation can be a 3D reconstruction, a set of images with poses tagged or a deep neural network.

This document might have some errors or missing parts. Feel free to make suggestions or pull request. All contributions are well appreciated.

## Table of Contents

- [Main challenges](#main-challenges)
- [Benchmark](#benchmark)
- [Challenges](#challenges)
- [Tutorial](#tutorial)
- [Category](#category)
- [Localization Component](#localization-component)
    - [Visual Feature](#visual-feature)
    - [Image Retrieval](#image-retrieval)
    - [Feature Match](#feature-match)
    - [Pose Computation](#pose-computation)
    - [Structure From Motion](#structure-from-motion)
- [Localization System](#localization-system)
    - [Structure-based](structure-based)
    - [Structure-based With Image Retrieval](#structure-based-with-image-retrieval)
    - [Scene Point Regression](#scene-point-regression)
    - [Absolute Pose Regression](#absolute-pose-regression)
    - [Pose Interpolation](#pose-interpolation)
    - [Relative Pose Estimation](#relative-pose-estimation)


## Main Challenges
- Illumination changes
- Dynamic scenes with moving objects
- Long-time period with different seasons
- Occlusion of the scene by an object or person
- Strong viewpoint difference

## Benchmark
- [LONG-TERM VISUAL LOCALIZATION](https://www.visuallocalization.net/)

## Challenges
- [2022 ECCV] [Map-Based Localization for Autonomous Driving](https://www.sites.google.com/view/mlad-eccv2022)
- [2021 ICCV] [Long-Term Visual Localization under Changing Conditions](https://sites.google.com/view/ltvl2021/home)
- [2021 ICCV] [Map-Based Localization for Autonomous Driving](https://sites.google.com/view/mlad-iccv2021)
- [2020 ECCV] [Long-Term Visual Localization under Changing Conditions](https://www.visuallocalization.net/workshop/eccv/2020/)
- [2020 ECCV] [Map-Based Localization for Autonomous Driving](https://sites.google.com/view/mlad-eccv2020/home)
- [2019 CVPR] [Long-Term Visual Localization under Changing Conditions](https://sites.google.com/view/ltvl2019/home)

## Tutorial
- [ICCV 2021 Large-Scale Visual Localization](https://sites.google.com/view/lsvpr2021/home)

## Category
|               Approach               | 3D map |                              Pros                              |                                                          Cons                                                         |
|:------------------------------------:|:------:|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| Structure-based                      | yes    | Perform very well in most scenarios                            | Challenging in large environments in terms of processing time and memory consumption                                  |
| Structure-based with image retrieval | yes    | Improve speed and robustness for large-scale settings          | Quality heavily relies on image retrieval                                                                             |
| Scene point regression               | yes/no | Very accurate position in small-scale settings                 | To be improved in large environments                                                                                  |
| Absolute pose regression             | no     | Fast pose approximation, can be trained for certain challenges | Low accuracy                                                                                                          |
| Pose interpolation                   | no     | Fast and lightweight                                           | Quality relies heavily on image retrieval and only provides a rough pose                                              |
| Relative pose estimation             | no     | Fast and lightweight                                           | Quality relies heavily on image retrieval and, e.g., local feature matches or a DNN used for relative pose estimation |


<br/><br/><br/>
<img src="https://europe.naverlabs.com/wp-content/uploads/2021/03/visual_localization_methods.png" width="800px">
<br/>
Image from https://europe.naverlabs.com/blog/methods-for-visual-localization/




## Localization Component

### Visual Feature
- [2020 CVPR] ASLFeat: Learning Local Features of Accurate Shape and Localization [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Luo_ASLFeat_Learning_Local_Features_of_Accurate_Shape_and_Localization_CVPR_2020_paper.pdf)
- [2020 ECCV] Learning Feature Descriptors Using Camera Pose Supervision [[paper]](https://arxiv.org/pdf/2004.13324.pdf?ref=https://githubhelp.com)
- [2019 NeurIPS] R2D2: Reliable and Repeatable Detector and Descriptor [[paper]](https://proceedings.neurips.cc/paper/2019/file/3198dfd0aef271d22f7bcddd6f12f5cb-Paper.pdf)
- [2019 CVPR] D2-Net: A Trainable CNN for Joint Description and Detection of Local Features [[paper]](https://openaccess.thecvf.com/content_CVPR_2019/papers/Dusmanu_D2-Net_A_Trainable_CNN_for_Joint_Description_and_Detection_of_CVPR_2019_paper.pdf)
- [2019 arXiv] From handcrafted to deep local features [[paper]](https://arxiv.org/pdf/1807.10254)
- [2018 CVPR] Semantic Visual Localization [[paper]](https://openaccess.thecvf.com/content_cvpr_2018/papers/Schonberger_Semantic_Visual_Localization_CVPR_2018_paper.pdf)
- [2018 CVPR] SuperPoint: Self-Supervised Interest Point Detection and Description [[paper]](https://openaccess.thecvf.com/content_cvpr_2018_workshops/papers/w9/DeTone_SuperPoint_Self-Supervised_Interest_CVPR_2018_paper.pdf)
- [2017 CVPR] Comparative Evaluation of Hand-Crafted and Learned Local Features [[paper]](https://openaccess.thecvf.com/content_cvpr_2017/papers/Schonberger_Comparative_Evaluation_of_CVPR_2017_paper.pdf)
- [2017 ICRA] Semantics-aware visual localization under challenging perceptual conditions [[paper]](https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?tp=&arnumber=7989305&ref=aHR0cHM6Ly9zY2hvbGFyLmdvb2dsZS5jby5qcC8=)
- [2004 IJCV] Distinctive Image Features from Scale-Invariant Keypoints [[paper]](https://link.springer.com/content/pdf/10.1023/B:VISI.0000029664.99615.94.pdf)

### Image Retrieval
- [2022 arXiv] Investigating the Role of Image Retrieval for Visual Localization -- An exhaustive benchmark [[paper]](https://arxiv.org/pdf/2205.15761)
- [2019 ICCV] Learning With Average Precision: Training Image Retrieval With a Listwise Loss [[paper]](https://openaccess.thecvf.com/content_ICCV_2019/papers/Revaud_Learning_With_Average_Precision_Training_Image_Retrieval_With_a_Listwise_ICCV_2019_paper.pdf)
- [2019 TPAMI] Fine-Tuning CNN Image Retrieval with No Human Annotation [[paper]](https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?tp=&arnumber=8382272&ref=aHR0cHM6Ly9pZWVleHBsb3JlLmllZWUub3JnL2Fic3RyYWN0L2RvY3VtZW50LzgzODIyNzI/Y2FzYV90b2tlbj1zMnlndGdkLUpYMEFBQUFBOmgtMm9Kb1NLT1dQZmZoMUlwRFJwTnVBbnVsUGhYLTRoNHVpNnlVMWY5VmZPOXgzMU05M1p6Y0pIcUo4aVNjVFJYcmlTREQybkkwT0NJTlE=)
- [2017 IJCV] End-to-End Learning of Deep Visual Representations for Image Retrieval [[paper]](https://link.springer.com/content/pdf/10.1007/s11263-017-1016-8.pdf)
- [2016 CVPR] NetVLAD: CNN Architecture for Weakly Supervised Place Recognition [[paper]](https://openaccess.thecvf.com/content_cvpr_2016/papers/Arandjelovic_NetVLAD_CNN_Architecture_CVPR_2016_paper.pdf)
- [2015 CVPR] 24/7 Place Recognition by View Synthesis [[paper]](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Torii_247_Place_Recognition_2015_CVPR_paper.pdf)

### Feature Match
- [2022 arXiv] Is Geometry Enough for Matching in Visual Localization? [[paper]](https://arxiv.org/pdf/2203.12979)
- [2021 CVPR] LoFTR: Detector-Free Local Feature Matching with Transformers [[paper]](https://arxiv.org/pdf/2104.00680.pdf) [[code]](https://github.com/zju3dv/LoFTR) [[project]](https://zju3dv.github.io/loftr/)
- [2020 ECCV] S2DNet : Learning Image Features for Accurate Sparse-to-Dense Matching [[paper]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123480630.pdf) [[code]](https://github.com/germain-hug/S2DNet-Minimal)
- [2020 CVPR] SuperGlue: Learning Feature Matching With Graph Neural Networks [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Sarlin_SuperGlue_Learning_Feature_Matching_With_Graph_Neural_Networks_CVPR_2020_paper.pdf)
- [2019 3DV] Sparse-to-Dense Hypercolumn Matching for Long-Term Visual Localization [[paper]](https://arxiv.org/pdf/1907.03965) [[code]](https://github.com/germain-hug/S2DHM)
- [2018 ECCV] Semantic Match Consistency for Long-Term Visual Localization [[paper]](https://openaccess.thecvf.com/content_ECCV_2018/papers/Carl_Toft_Semantic_Match_Consistency_ECCV_2018_paper.pdf)
- [2017 TPAMI] Efficient amp; Effective Prioritized Matching for Large-Scale Image-Based Localization [[paper]](https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?tp=&arnumber=7572201&ref=aHR0cHM6Ly9zY2hvbGFyLmdvb2dsZS5jby5qcC8=)
- [2017 ICCV] Efficient Global 2D-3D Matching for Camera Localization in a Large-Scale 3D Map [[paper]](https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?tp=&arnumber=8237522&ref=aHR0cHM6Ly9pZWVleHBsb3JlLmllZWUub3JnL2RvY3VtZW50LzgyMzc1MjI=)
- [2014 3DV] Matching Features Correctly through Semantic Understanding [[paper]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7035860)
- [2008 TPAMI] Optimal Randomized RANSAC [[paper]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4359381)
- [1981 CACM] Random sample consensus: a paradigm for model fitting with applications to image analysis and automated cartography [[paper]](https://dl.acm.org/doi/pdf/10.1145/358669.358692)

### Pose Computation
- [2022 CVPR] The Probabilistic Normal Epipolar Constraint for Frame-To-Frame Rotation Optimization under Uncertain Feature Positions [[paper]](https://openaccess.thecvf.com/content/CVPR2022/papers/Muhle_The_Probabilistic_Normal_Epipolar_Constraint_for_Frame-to-Frame_Rotation_Optimization_Under_CVPR_2022_paper.pdf)
- [2020 ECCV] Solving the Blind Perspective-n-Point Problem End-To-End With Robust Differentiable Geometric Optimization [[paper]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123470239.pdf) [[code]](https://github.com/dylan-campbell/bpnpnet)
- [2011 CVPR] A novel parametrization of the perspective-three-point problem for a direct computation of absolute camera position and orientation [[paper]](https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?tp=&arnumber=5995464&ref=aHR0cHM6Ly9pZWVleHBsb3JlLmllZWUub3JnL2RvY3VtZW50LzU5OTU0NjQ=)

### Structure From Motion
- [2016 CVPR] Structure-from-Motion Revisited [[paper]](https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?tp=&arnumber=7780814&ref=aHR0cHM6Ly9pZWVleHBsb3JlLmllZWUub3JnL2RvY3VtZW50Lzc3ODA4MTQ=)
- [2013 ICCV] Global Fusion of Relative Motions for Robust, Accurate and Scalable Structure from Motion [[paper]](https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?tp=&arnumber=6751515&ref=aHR0cHM6Ly9pZWVleHBsb3JlLmllZWUub3JnL2RvY3VtZW50LzY3NTE1MTU=)

## Localization System

### Structure-based
- [2021 CVPR] Back to the Feature: Learning Robust Camera Localization from Pixels to Pose [[paper]](https://openaccess.thecvf.com/content/CVPR2021/papers/Sarlin_Back_to_the_Feature_Learning_Robust_Camera_Localization_From_Pixels_CVPR_2021_paper.pdf) [[code]](https://github.com/cvg/pixloc)
- [2019 CVPR] Visual Localization by Learning Objects-Of-Interest Dense Match Regression [[paper]](https://openaccess.thecvf.com/content_CVPR_2019/papers/Weinzaepfel_Visual_Localization_by_Learning_Objects-Of-Interest_Dense_Match_Regression_CVPR_2019_paper.pdf)
- [2018 CVPR] InLoc: Indoor Visual Localization with Dense Matching and View Synthesis [[paper]](https://openaccess.thecvf.com/content_cvpr_2018/papers/Taira_InLoc_Indoor_Visual_CVPR_2018_paper.pdf) [[code]](https://github.com/HajimeTaira/InLoc_demo)
- [2011 ICCV] Fast Image-Based Localization using Direct 2D-to-3D Matching [[paper]](https://www.graphics.rwth-aachen.de/media/papers/sattler_iccv11_preprint_011.pdf)

### Structure-based With Image Retrieval
- [2022 arXiv] Robust Image Retrieval-based Visual Localization using Kapture [[paper]](https://arxiv.org/pdf/2007.13867.pdf) [[code]](https://github.com/naver/kapture-localization)
- [2020 ECCV Workshop] Hierarchical Localization with hloc and SuperGlue [[slides]](https://psarlin.com/assets/talks/hloc+SuperGlue_15min_ltvl_slides.pdf) [[code]](https://github.com/cvg/Hierarchical-Localization)
- [2019 CVPR] From Coarse to Fine: Robust Hierarchical Localization at Large Scale [[paper]](https://openaccess.thecvf.com/content_CVPR_2019/papers/Sarlin_From_Coarse_to_Fine_Robust_Hierarchical_Localization_at_Large_Scale_CVPR_2019_paper.pdf) [[code]](https://github.com/ethz-asl/hfnet)

### Scene Point Regression
- [2021 TPAMI] Visual Camera Re-Localization from RGB and RGB-D Images Using DSAC [[paper]](https://arxiv.org/pdf/2002.12324.pdf) [[code]](https://github.com/vislearn/dsacstar)
- [2020 CVPR] Hierarchical Scene Coordinate Classification and Regression for Visual Localization [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Li_Hierarchical_Scene_Coordinate_Classification_and_Regression_for_Visual_Localization_CVPR_2020_paper.pdf) [[code]](https://github.com/AaltoVision/hscnet)
- [2019 ICCV] SANet: Scene Agnostic Network for Camera Localization [[paper]](https://openaccess.thecvf.com/content_ICCV_2019/papers/Yang_SANet_Scene_Agnostic_Network_for_Camera_Localization_ICCV_2019_paper.pdf) [[code]](https://github.com/sfu-gruvi-3dv/sanet_relocal_demo)
- [2019 ICCV] Expert Sample Consensus Applied to Camera Re-Localization [[paper]](https://openaccess.thecvf.com/content_ICCV_2019/papers/Brachmann_Expert_Sample_Consensus_Applied_to_Camera_Re-Localization_ICCV_2019_paper.pdf) [[code]](https://github.com/vislearn/esac)
- [2018 CVPR] Learning Less is More – 6D Camera Localization via 3D Surface Regression [[paper]](https://openaccess.thecvf.com/content_cvpr_2018/papers/Brachmann_Learning_Less_Is_CVPR_2018_paper.pdf) [[code]](https://github.com/vislearn/LessMore)
- [2017 CVPR] DSAC - Differentiable RANSAC for Camera Localization [[paper]](https://openaccess.thecvf.com/content_cvpr_2017/papers/Brachmann_DSAC_-_Differentiable_CVPR_2017_paper.pdf) [[code]](https://github.com/cvlab-dresden/DSAC)
- [2013 CVPR] Scene Coordinate Regression Forests for Camera Relocalization in RGB-D Images [[paper]](https://openaccess.thecvf.com/content_cvpr_2013/papers/Shotton_Scene_Coordinate_Regression_2013_CVPR_paper.pdf)

### Absolute Pose Regression
- [2018 ICRA] Deep Auxiliary Learning for Visual Localization and Odometry [[paper]](https://arxiv.org/pdf/1803.03642.pdf)
- [2018 RA-L] VLocNet++: Deep Multitask Learning for Semantic Visual Localization and Odometry [[paper]](https://arxiv.org/pdf/1804.08366.pdf)
- [2018 CVPR] Geometry-Aware Learning of Maps for Camera Localization [[paper]](https://openaccess.thecvf.com/content_cvpr_2018/papers/Brahmbhatt_Geometry-Aware_Learning_of_CVPR_2018_paper.pdf) [[code]](https://github.com/NVlabs/geomapnet)
- [2017 CVPR] Image-based localization using LSTMs for structured feature correlation [[paper]](https://openaccess.thecvf.com/content_ICCV_2017/papers/Walch_Image-Based_Localization_Using_ICCV_2017_paper.pdf)
- [2017 CVPR] Geometric loss functions for camera pose regression with deep learning [[paper]](https://openaccess.thecvf.com/content_cvpr_2017/papers/Kendall_Geometric_Loss_Functions_CVPR_2017_paper.pdf)
- [2015 ICCV] PoseNet: A Convolutional Network for Real-Time 6-DOF Camera Relocalization [[paper]](https://openaccess.thecvf.com/content_iccv_2015/papers/Kendall_PoseNet_A_Convolutional_ICCV_2015_paper.pdf)

### Pose Interpolation
- [2019 CVPR] Understanding the Limitations of CNN-based Absolute Camera Pose Regression [[paper]](https://openaccess.thecvf.com/content_CVPR_2019/papers/Sattler_Understanding_the_Limitations_of_CNN-Based_Absolute_Camera_Pose_Regression_CVPR_2019_paper.pdf)
- [2011 ICCV Workshop] Visual localization by linear combination of image descriptors [[paper]](https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?tp=&arnumber=6130230&ref=aHR0cHM6Ly9pZWVleHBsb3JlLmllZWUub3JnL2RvY3VtZW50LzYxMzAyMzA=)

### Relative Pose Estimation
- [2020 ICRA] To Learn or Not to Learn: Visual Localization from Essential Matrices [[paper]](https://arxiv.org/pdf/1908.01293.pdf)
- [2019 ICCV] CamNet: Coarse-to-Fine Retrieval for Camera Re-Localization [[paper]](https://openaccess.thecvf.com/content_ICCV_2019/papers/Ding_CamNet_Coarse-to-Fine_Retrieval_for_Camera_Re-Localization_ICCV_2019_paper.pdf)
- [2018 ECCV] RelocNet: Continuous Metric Learning Relocalisation using Neural Nets [[paper]](https://openaccess.thecvf.com/content_ECCV_2018/papers/Vassileios_Balntas_RelocNet_Continous_Metric_ECCV_2018_paper.pdf) 
- [2017 ICCV Workshop] Camera Relocalization by Computing Pairwise Relative Poses Using Convolutional Neural Network [[paper]](https://openaccess.thecvf.com/content_ICCV_2017_workshops/papers/w17/Laskar_Camera_Relocalization_by_ICCV_2017_paper.pdf) [[code]](https://github.com/AaltoVision/camera-relocalisation)
- [2006 3DPVT] Image Based Localization in Urban Environments [[paper]](https://web.archive.org/web/20130512063647id_/http://www.cs.gmu.edu:80/~wzhang2/publication/Localization1.pdf)

