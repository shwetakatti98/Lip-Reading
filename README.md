## ECE 209AS - PROJECT

This repo contains project details for ECE 209AS Lip Reading Project. This project is done under Prof. Mani Srivastava during the Spring Quarter in UCLA (academic year: 2021 - 2022).

## Team Members
1. Shweta Katti (UID: 505604846) - shwetakatti@g.ucla.edu
2. Amulya Shruthi Tammireddi (UID: 505626283) - ashruthi1797@g.ucla.edu


## Code Base
All code changes can be found along the path https://github.com/shwetakatti98/Lip-Reading


## 1. Motivation & Objective

The aim of this project is to provide a comparative analysis on the various lip reading techniques available and maximizing efficiency of detection on existing video datasets. This project will provide a comprehensive guide for the methods currently in use and evaluate the performance.

## 2. State of the Art & Its Limitations

There are several State of the Art methods available today but there is no specific guide comparing the available models to select the most accurate based on the dataset and Feature Extraction.

## 3. Novelty & Rationale

In this project, our focus is on the challenges encountered in a lip reading task, especially those concerning dataset and feature extraction. Existing surveys have only reviewed a few topics and mainly focus on the comparison of various methods and their performance on a specific dataset for a specific task. This project aims to review the various datasets available for each of the current widely used models. For selecting our models and datasets we conducted a literature survey to shortlist the primary architectures that can be chosen for the detection.

## 4. Potential Impact

This project can primarily help in the following usecases :

- Lip reading mainly helps those people with hearing loss. It aids them in comprehending speech clearly. <br>
- It also helps people work in situations where the background is noisy and assists them in interpreting speech.<br>
- A lot of lip reading softwares used in public places like kiosks and ATMs can help people have contactless interactions and ensure privacy , since it doesn't involve speaking out loud.<br>

By performing a comparative analysis between various models and nets we can maximize efficiency for these use cases.

## 5. Challenges

Lip reading is an extremely challenging task by itself. On the other hand, there are variety of factors making test videos different from development data, and consequently overshadowing the accuracy and performance of lip reading systems. We plan to review both Data Challenges and Model Implementation and accuracy challenges through this paper's comparative analysis.

## 6. Requirements for Success
To compare the identified models with the evaluation metrics and to find the best performing architecture. 

## 7. Metrics of Success
Various metrics have been utilized to evaluate the performance of Visual Speech recognition systems, including word accuracy and Sentence Accuracy Rate (SAR). We plan on utilizing Error Rate (ER) metrics on different levels such as word, character, etc. as our evaluation criteria.

## 8. Execution Plan
- Implementing the models
- Training the models with the chosen datasets
- Testing the models and evaluating the metrics
- Comparing the various architectures selected

The chosen models will be divided between both the team members to implement and train.

## 9. Related Work

### 9.a. Papers
Out of the 20+ papers studied, we selected the following as our base papers to begin with the comparitive analysis of the best architecture:
| Paper citation| Methodology|
| --- | --- |
|Lip reading sentences in the wild [1] |‘Watch, Listen, Attend and Spell’ (WLAS) network:The convolutional network is based on the VGG-M model, followed by LSTM encoder and transducer.|
|Lipnet: End-to-end sentence-level lipreading [2] |LipNet - CNN+BiGRU+CTC loss |
|The conversation: Deep audio-visual speech enhancement [3] | The network consists of a 3D convolution layer, followed by a 18-layer ResNet. |
|Recent advances in the automatic recognition of audiovisual speech [4] | MLLR, MAP, HMMs |
|Improved speaker independent lip reading using speaker adaptive training and deep neural networks [5] | Error rates reduced by using Context - Dependent DNN architectures |

### 9.b. Datasets

Lip reading datasets can be classified into two categories: 
- Lip Reading in Controlled Environments
- Lip Reading in the Wild

The datasets we are working with include -
-  Lip Reading in the Wild: LRW
-  LRS2-BBC
-  LRS3-TED
-  Multi-View Lip Reading Sentences (MV-LRS)
-  Large-Scale Visual Speech Recognition(LSVSR).
-  GRID

### 9.c. Software
The softwares we plan to use but are not limited to include Python, Jupyter Notebooks and Google Colab.

## 10. References

[1] Chung, Joon Son, et al. "Lip reading sentences in the wild." 2017 IEEE conference on computer vision and pattern recognition (CVPR). IEEE, 2017. <br>
[2] Assael, Yannis M., et al. "Lipnet: End-to-end sentence-level lipreading." arXiv preprint arXiv:1611.01599 (2016). <br>
[3] Afouras, Triantafyllos, Joon Son Chung, and Andrew Zisserman. "The conversation: Deep audio-visual speech enhancement." arXiv preprint arXiv:1804.04121 (2018). <br>
[4] G. Potamianos, C. Neti, G. Gravier, A. Garg and A. W. Senior, "Recent advances in the automatic recognition of audiovisual speech," in Proceedings of the IEEE, vol. 91, no. 9, pp. 1306-1326, Sept. 2003, doi: 10.1109/JPROC.2003.817150. <br>
[5] Almajai, I., Cox, S., Harvey, R. and Lan, Y., 2016, March. Improved speaker independent lip reading using speaker adaptive training and deep neural networks. In 2016 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP) (pp. 2722-2726). IEEE. <br>
[6]Joon Son Chung and Andrew Zisserman. Lip reading in the wild. In Asian conference on computer vision, pages 87–103. Springer, 2016. <br>
[7] Triantafyllos Afouras, Joon Son Chung, and Andrew Zisserman. Lrs3-ted: a large-scale dataset for visual speech recognition. arXiv preprint arXiv:1809.00496, 2018. <br>
[8]  Brendan Shillingford, Yannis Assael, Matthew W Hoffman, Thomas Paine, Cían Hughes, Utsav Prabhu, Hank Liao, Hasim Sak, Kanishka Rao, Lorrayne Bennett, et al. Large-scale visual speech recognition. arXiv preprint arXiv:1807.05162, 2018.<br>
[9] Joon Son Chung and AP Zisserman. Lip reading in profile. 2017 <br>

