# Deep Audio-Visual Speech Recognition


## Requirements

System packages:

	ffmpeg==2.8.15
	python==3.6.9

Python packages:

	editdistance==0.5.3
	matplotlib==3.1.1
	numpy==1.18.1
	opencv-python==4.2.0
	pytorch==1.2.0
	scipy==1.3.1
	tqdm==4.42.1

CUDA 10.0 (if NVIDIA GPU is to be used):

	cudatoolkit==10.0



#### Directories

`/checkpoints`: Temporary directory to store intermediate model weights and plots while training. Gets automatically created.

`/data`: Directory containing the LRS2 Main and Pretrain dataset class definitions and other required data-related utility functions.

`/final`: Directory to store the final trained model weights and plots. If available, place the pre-trained model weights in the `models` subdirectory.

`/models`: Directory containing the class definitions for the models.

`/utils`: Directory containing function definitions for calculating CER/WER, greedy search/beam search decoders and preprocessing of data samples. Also contains functions to train and evaluate the model.

#### Files

`checker.py`: File containing checker/debug functions for testing all the modules and the functions in the project as well as any other checks to be performed.

`config.py`: File to set the configuration options and hyperparameter values.

`demo.py`: Python script for generating predictions with the specified trained model for all the data samples in the specified demo directory.

`preprocess.py`: Python script for preprocessing all the data samples in the dataset.

`pretrain.py`: Python script for pretraining the model on the pretrain set of the LRS2 dataset using curriculum learning.

`test.py`: Python script to test the trained model on the test set of the LRS2 dataset.

`train.py`: Python script to train the model on the train set of the LRS2 dataset.



## Pre-trained Weights

Download the pre-trained weights for the Visual Frontend from [here](https://drive.google.com/file/d/1cgpu3X6WFbkrMDaHGX-8SWzj4gS-lU6s/view?usp=drivesdk) and for the Language Model from [here](https://drive.google.com/file/d/19viuy3ZXDkmigzdEiRGSZZG1TXwqw3Tb/view?usp=drivesdk). Once the Visual Frontend and Language Model weights are downloaded, place them in a folder and add their paths in the `config.py` file.




#### Inference

1. Set the configuration options in the `config.py` file. Comments have been provided for each option.

2. Run the `demo.py` script to use the model to make predictions for each sample in a demo directory. Read the specifications for the sample in the `demo.py` file.



## References

1. The pre-trained weights of the Visual Frontend and the Language Model have been obtained from [Afouras T. and Chung J, Deep Lip Reading: a comparison of models and an online application, 2018](https://github.com/afourast/deep_lip_reading) GitHub repository.

2. The CTC beam search implementation is adapted from [Harald Scheidl, CTC Decoding Algorithms](https://github.com/githubharald/CTCDecoder) GitHub repository.


