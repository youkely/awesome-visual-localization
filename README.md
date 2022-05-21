# Awesome Visual Localization

A literature review on the research of visual localization, i.e. estimate the 6 dof pose of an image given a representation of the world created using a set of reference images. The representation can be a 3D reconstruction, a set of images with poses tagged or a deep neural network.

This document might has some errors or missing parts. Feel free to make suggestions or pull request. All contributions are well appreciated.

## Table of Contents

- [Main challenges](#main-challenges)
- [Benchmark](#benchmark)
- [Tutorial](#tutorial)
- [Category](#category)
- [Localization Component](#localization-component)
    - [Visual Feature](#visual-feature)
    - [Feature Match](#feature-match)
- [Localization System](#localization-system)


## Main Challenges
- Illumination changes
- Dynamic scenes with moving objects
- Long-time period with different seasons
- Occlusion of the scene by an object or person
- Strong viewpoint difference

## Benchmark
- [LONG-TERM VISUAL LOCALIZATION](https://www.visuallocalization.net/)

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
<img src="https://europe.naverlabs.com/wp-content/uploads/2021/03/visual_localization_methods.png" width="400px">
<font size=4>Image from https://europe.naverlabs.com/blog/methods-for-visual-localization/</font>




## Localization Component

### Visual Feature
- [2019 NeurIPS] R2D2: Reliable and Repeatable Detector and Descriptor [[paper]](https://proceedings.neurips.cc/paper/2019/file/3198dfd0aef271d22f7bcddd6f12f5cb-Paper.pdf)
- [2019 CVPR] D2-Net: A Trainable CNN for Joint Description and Detection of Local Features [[paper]](https://openaccess.thecvf.com/content_CVPR_2019/papers/Dusmanu_D2-Net_A_Trainable_CNN_for_Joint_Description_and_Detection_of_CVPR_2019_paper.pdf)
- [2019 arXiv] From handcrafted to deep local features [[paper]](https://arxiv.org/pdf/1807.10254)
- [2018 CVPR] SuperPoint: Self-Supervised Interest Point Detection and Description [[paper]](https://openaccess.thecvf.com/content_cvpr_2018_workshops/papers/w9/DeTone_SuperPoint_Self-Supervised_Interest_CVPR_2018_paper.pdf)
- [2017 CVPR] Comparative Evaluation of Hand-Crafted and Learned Local Features [[paper]](https://openaccess.thecvf.com/content_cvpr_2017/papers/Schonberger_Comparative_Evaluation_of_CVPR_2017_paper.pdf)
- [2017 ICRA] Semantics-aware visual localization under challenging perceptual conditions [[paper]](https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?tp=&arnumber=7989305&ref=aHR0cHM6Ly9zY2hvbGFyLmdvb2dsZS5jby5qcC8=)
- [2004 IJCV] Distinctive Image Features from Scale-Invariant Keypoints [[paper]](https://link.springer.com/content/pdf/10.1023/B:VISI.0000029664.99615.94.pdf)

### Feature Match

## Localization System

###
