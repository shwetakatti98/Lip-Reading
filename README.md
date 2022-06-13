## ECE 209AS - PROJECT

This repo contains project details for ECE 209AS Lip Reading Project. This project is done under Prof. Mani Srivastava during the Spring Quarter in UCLA (academic year: 2021 - 2022).


## Team Members
1. Shweta Katti (UID: 505604846) - shwetakatti@g.ucla.edu
2. Amulya Shruthi Tammireddi (UID: 505626283) - ashruthi1797@g.ucla.edu


## Code Base
All code changes can be found along the path https://github.com/shwetakatti98/Lip-Reading


## 1. Motivation & Objective
Lip reading refers to understanding speech or words based on analysing the speakers lip movements to interpret the content. It is also known as Visual Speech Recognition. 
<br>
- The overall goal of this project is to provide a comparative analysis on the various lip-reading techniques available and explore the various architectures.

- Our aim was to test several popular models and architectures available for lip reading and conduct a survey to analyze their performance on a given test dataset.

- We selected a combination of popular and relatively new architectures based on our literature survey and obtained their pre-trained weights for evaluation.

- Utilized various metrics to understand which of the implemented models perform the best given a particular dataset.

## 2. State of the Art & Its Limitations

There are several State of the Art methods available today but there is no specific guide comparing the available models to select the most accurate based on the dataset and Feature Extraction.

LIMITATIONS:
- Each of the proposed works available provides results of training and testing on a specific dataset.
- No survey available till date which tests on a specific dataset and compares the models.

## 3. Novelty & Rationale

In this project, our focus is on the challenges encountered in a lip reading task, especially those concerning dataset and feature extraction. Existing surveys have only reviewed a few topics and mainly focus on the comparison of various methods and their performance on a specific dataset for a specific task. This project aims to review the various datasets available for each of the current widely used models. For selecting our models and datasets we conducted a literature survey to shortlist the primary architectures that can be chosen for the detection.
Novelty of the project includes -
- We test our choice of models on the same test dataset, in our case the LRW dataset. 
- We find the Error Rates for evaluating and comparing the models.


## 4. Potential Impact

This project can primarily help in the following usecases :

- Lip reading mainly helps those people with hearing loss. It aids them in comprehending speech clearly. <br>
- It also helps people work in situations where the background is noisy and assists them in interpreting speech.<br>
- A lot of lip reading softwares used in public places like kiosks and ATMs can help people have contactless interactions and ensure privacy , since it doesn't involve speaking out loud.<br>

By performing a comparative analysis between various models and nets we can maximize efficiency for these use cases.

## 5. Challenges

Lip reading is an extremely challenging task by itself. Training the models and testingthem accurately on the same chosen dataset is chalenging. On the other hand, there are variety of factors making test videos different from development data, and consequently overshadowing the accuracy and performance of lip reading systems. 

## 6. Requirements for Success
To compare the identified models with the evaluation metrics and to find the best performing architecture. 

## 7. Metrics of Success
Various metrics have been utilized to evaluate the performance of Visual Speech recognition systems, including word accuracy and Sentence Accuracy Rate (SAR). We plan on utilizing Error Rate (ER) metric on the word level (WER) as the evaluation criteria.

## 8. Execution Plan
- Implementing the models
- Training the models with the chosen datasets
- Testing the models and evaluating the metrics
- Comparing the various architectures selected

The chosen models will be divided between both the team members to implement and train.

## 9. Related Work

### 9.a. Literature review
We performed a review of around 20+ papers to understand current models, architectures and corresponding datasets used for visual speech recognition. The link to the literarture review sheet is as follows :
https://docs.google.com/spreadsheets/d/137hSvHNE2dYTGoN9PBO9bHsO_sFK0LwsScMN_iWpnRs/edit#gid=0


### 9.c. Datasets

Lip reading datasets can be classified into two categories: 
- Lip Reading in Controlled Environments
- Lip Reading in the Wild

The datasets we are working with include -
-  Lip Reading in the Wild: LRW
-  LRS2-BBC
-  LRS
-  GRID Corpus

### 9.d. Software
The softwares we plan to use include Python, Jupyter Notebooks and Google Colab.

## 10. Summary of Models chosen
Out of the 20+ papers studied, we selected the following as our base papers to begin with the comparative analysis of the best architecture. The pre-trained weights and training/testing steps are given in the links for each of the model's code (provided under the Readme.md file)
| Paper citation                | Architecture         | Dataset  | Preprocessing | Pre-trained weights | Word Error Rate|Code Link|
| -------------------------------------------------- | -----------------------------|----------|---------------|---------------------|----------------| -------- |
|Assael, Yannis M., et al. "Lipnet: End-to-end sentence-level lipreading." arXiv preprint arXiv:1611.01599 (2016).|LipNet - CNN+BiGRU+CTC loss | GRID Corpus |D-lib for face detection, data augmentation | Weights available online | 26.3% | https://github.com/shwetakatti98/Lip-Reading/tree/main/LipNet|
|B. Martinez, P. Ma, S. Petridis and M. Pantic, "Lipreading Using Temporal Convolutional Networks," ICASSP 2020 - 2020 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2020, pp. 6319-6323, doi: 10.1109/ICASSP40776.2020.9053841| The network consists of a 3D convolution layer, followed by a 18-layer ResNet and a Temporal Convolution Network | LRW BBC dataset | SSD face detection, pre-training and data augmentation | Weights available online | 12% | https://github.com/shwetakatti98/Lip-Reading/tree/main/Lipreading_using_Temporal_Convolutional_Networks |
|Stafylakis, Themos & Tzimiropoulos, Georgios. (2017). Combining Residual Networks with LSTMs for Lipreading| Spatiotemporal convolution + ResNet + Bidirectional LSTM + Softmax layer| LRW BBC dataset| Detections of landmarks + cropping of ROI + conversion to grayscale| Trained on the lab GPU| 24.3%| https://github.com/shwetakatti98/Lip-Reading/tree/main/Lipreading-ResNet |
| Afouras, Triantafyllos & Chung, Joon Son & Senior, Andrew & Vinyals, Oriol & Zisserman, Andrew. (2018). Deep Audio-visual Speech Recognition. IEEE Transactions on Pattern Analysis and Machine Intelligence. PP. 1-1. 10.1109/TPAMI.2018.2889052. | TM - CTC model - Self-attention-based encoder architecture| LRS2-BBC | SSD face detection, pre-training and data augmentation |Pre-trained weights available online| 57.2% | https://github.com/shwetakatti98/Lip-Reading/tree/main/deep_avsr |
|Chung, Joon Son, et al. "Lip reading sentences in the wild." 2017 IEEE conference on computer vision and pattern recognition (CVPR). IEEE, 2017.|‘Watch, Listen, Attend and Spell’ (WLAS) network:The convolutional network is based on the VGG-M model, followed by LSTM encoder and transducer.| LRS Dataset | HOG face detection, landmark detection and data augmentation | Must be trained| Could not be trained or tested successfully | https://github.com/shwetakatti98/Lip-Reading/tree/main/WLAS |

## 11. Future Work
1. We can incorporate more personalized videos into the dataset for testing the models.
2. We can check how the models performance varies when multiple datasets are combined and used for training.
3. We can incorporate other evaluation metrics such as CER or SER.

## 12. References

[1] Chung, Joon Son, et al. "Lip reading sentences in the wild." 2017 IEEE conference on computer vision and pattern recognition (CVPR). IEEE, 2017. <br>
[2] Assael, Yannis M., et al. "Lipnet: End-to-end sentence-level lipreading." arXiv preprint arXiv:1611.01599 (2016). <br>
[3] Afouras, Triantafyllos, Joon Son Chung, and Andrew Zisserman. "The conversation: Deep audio-visual speech enhancement." arXiv preprint arXiv:1804.04121 (2018). <br>
[4] G. Potamianos, C. Neti, G. Gravier, A. Garg and A. W. Senior, "Recent advances in the automatic recognition of audiovisual speech," in Proceedings of the IEEE, vol. 91, no. 9, pp. 1306-1326, Sept. 2003, doi: 10.1109/JPROC.2003.817150. <br>
[5] Almajai, I., Cox, S., Harvey, R. and Lan, Y., 2016, March. Improved speaker independent lip reading using speaker adaptive training and deep neural networks. In 2016 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP) (pp. 2722-2726). IEEE. <br>
[6]Joon Son Chung and Andrew Zisserman. Lip reading in the wild. In Asian conference on computer vision, pages 87–103. Springer, 2016. <br>
[7] Triantafyllos Afouras, Joon Son Chung, and Andrew Zisserman. Lrs3-ted: a large-scale dataset for visual speech recognition. arXiv preprint arXiv:1809.00496, 2018. <br>
[8]  Brendan Shillingford, Yannis Assael, Matthew W Hoffman, Thomas Paine, Cían Hughes, Utsav Prabhu, Hank Liao, Hasim Sak, Kanishka Rao, Lorrayne Bennett, et al. Large-scale visual speech recognition. arXiv preprint arXiv:1807.05162, 2018.<br>
[9] Joon Son Chung and AP Zisserman. Lip reading in profile. 2017 <br>

