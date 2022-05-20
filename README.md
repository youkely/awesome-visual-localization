# Awesome Visual Localization

A literature review on the research of visual localization, i.e. estimate the 6 dof pose of an image given a representation of the world created using a set of reference images. The representation can be a 3D reconstruction, a set of images with poses tagged or a deep neural network.

Main challenges for current methods consists of
- Illumination changes
- Dynamic scenes with moving objects
- Long-time period with different seasons
- Occlusion of the scene by an object or person
- Strong viewpoint difference

Some benchmark
- [LONG-TERM VISUAL LOCALIZATION](https://www.visuallocalization.net/)

Some tutorial
- [ICCV 2021 Large-Scale Visual Localization](https://sites.google.com/view/lsvpr2021/home)

Category：
![image](https://europe.naverlabs.com/wp-content/uploads/2021/03/visual_localization_methods.png)
|               Approach               | 3D map |                              Pros                              |                                                          Cons                                                         |
|:------------------------------------:|:------:|:--------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| Structure-based                      | yes    | Perform very well in most scenarios                            | Challenging in large environments in terms of processing time and memory consumption                                  |
| Structure-based with image retrieval | yes    | Improve speed and robustness for large-scale settings          | Quality heavily relies on image retrieval                                                                             |
| Scene point regression               | yes/no | Very accurate position in small-scale settings                 | To be improved in large environments                                                                                  |
| Absolute pose regression             | no     | Fast pose approximation, can be trained for certain challenges | Low accuracy                                                                                                          |
| Pose interpolation                   | no     | Fast and lightweight                                           | Quality relies heavily on image retrieval and only provides a rough pose                                              |
| Relative pose estimation             | no     | Fast and lightweight                                           | Quality relies heavily on image retrieval and, e.g., local feature matches or a DNN used for relative pose estimation |

## Table of Contents

- [Learning-based Approaches](#learning-based-approaches)
- [Structure-based Approaches](#structure-based-approaches)



## Learning-based Approaches

## Structure-based Approaches
