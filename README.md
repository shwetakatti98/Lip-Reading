## ECE 209AS - PROJECT

This repo contains project details for ECE 209AS Lip Reading Project. This project is done under Prof. Mani Srivastava during the Spring Quarter in UCLA (academic year: 2021 - 2022).

# Team Members
1. Shweta Katti (UID: 505604846) - shwetakatti@g.ucla.edu
2. Amulya Shruthi Tammireddi (UID: 505626283) - ashruthi1797@g.ucla.edu


# Code Base
All code changes can be found along the path https://github.com/shwetakatti98/Lip-Reading


## 1. Motivation & Objective

The aim of this project is to provide a comparative analysis on the various lip reading techniques available and maximizing efficiency of detection on existing video datasets. This project will provide a comprehensive guide for the methods currently in use and evaluate the performance.

## 2. State of the Art & Its Limitations

There are several State of the Art methods available today but there is no specific guide comparing the available models to select the most accurate based on the dataset and Feature Extraction.

## 3. Novelty & Rationale

In this project, our focus is on the challenges faced in automatic lip reading, especially those concerning dataset and feature extraction. Existing surveys of Visual Speech Recognition(VSR) have only reviewed a few topics and mainly focus on the comparison of various methods and their performance on a specific dataset for a specific task. This project aims to review the various datasets available for each of the current widely used models. For selecting our models we conducted a literature survey to shortlist the primary architectures that can be chosen for the detection.

## 4. Potential Impact

If the project is successful, what difference will it make, both technically and broadly?

## 5. Challenges

What are the challenges and risks?

## 6. Requirements for Success

What skills and resources are necessary to perform the project?

## 7. Metrics of Success

What are metrics by which you would check for success?

## 8. Execution Plan

Describe the key tasks in executing your project, and in case of team project describe how will you partition the tasks.

## 9. Related Work

### 9.a. Papers
Out of the 20+ papers studied, we selected the following as our base papers to begin with the comparitive analysis of the best architecture:
| Paper citation| Methodology|
| --- | --- |
|Chung, Joon Son, et al. "Lip reading sentences in the wild." 2017 IEEE conference on computer vision and pattern recognition (CVPR). IEEE, 2017.|‘Watch, Listen, Attend and Spell’ (WLAS) network:The convolutional network is based on the VGG-M model, followed by LSTM encoder and transducer.|
|Assael, Yannis M., et al. "Lipnet: End-to-end sentence-level lipreading." arXiv preprint arXiv:1611.01599 (2016).|LipNet - CNN+BiGRU+CTC loss |
|Afouras, Triantafyllos, Joon Son Chung, and Andrew Zisserman. "The conversation: Deep audio-visual speech enhancement." arXiv preprint arXiv:1804.04121 (2018).| The network consists of a 3D convolution layer, followed by a 18-layer ResNet. |
|G. Potamianos, C. Neti, G. Gravier, A. Garg and A. W. Senior, "Recent advances in the automatic recognition of audiovisual speech," in Proceedings of the IEEE, vol. 91, no. 9, pp. 1306-1326, Sept. 2003, doi: 10.1109/JPROC.2003.817150. | MLLR, MAP, HMMs |
|Almajai, I., Cox, S., Harvey, R. and Lan, Y., 2016, March. Improved speaker independent lip reading using speaker adaptive training and deep neural networks. In 2016 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP) (pp. 2722-2726). IEEE. | Error rates reduced by using Context - Dependent DNN architectures |

### 9.b. Datasets

List datasets that you have identified and plan to use. Provide references (with full citation in the References section below).

### 9.c. Software

List softwate that you have identified and plan to use. Provide references (with full citation in the References section below).

## 10. References

List references correspondign to citations in your text above. For papers please include full citation and URL. For datasets and software include name and URL.

