Lip Reading in the Wild using ResNet and LSTMs in Torch
=======================================================


## Requirements
See the [installation instructions](INSTALL.md) for a step-by-step guide.
- Install [Torch](http://torch.ch/docs/getting-started.html) on a machine with CUDA GPU
- Install [cuDNN v4 or v5](https://developer.nvidia.com/cudnn) and the Torch [cuDNN bindings](https://github.com/soumith/cudnn.torch/tree/R4)
- Install [rnn](https://github.com/Element-Research/rnn) (not tested with more recent versions).
- Download the [Lip Reading in the Wild](https://www.robots.ox.ac.uk/~vgg/data/lip_reading/) dataset

## Training

The training scripts come with several options, which can be listed with the `--help` flag.

This is the suggested order to train the models:

(i) Start by training a model with temporal convolutional backend (set `-netType 'temp_conv'`). Set `-LR 0.003` and let it for about 30 epochs.
(ii) Throw away the temporal convolutional backend, freeze the parameters of the frontend and the ResNet and train the LSTM backend (set `-netType 'LSTM_init'`). 5 epochs are enough to get a sensible initialization of the LSTM. Set `-LR 0.003`
(iii) Train the whole network end-to-end (set `-netType 'LSTM'`). In this case, set `-LR 0.0005` and about 30 epochs.


All these steps are performed (semi-)automatically by the code. You should (a) change the `netType` and `LR` parameters and (b) set the `retrain` parameter to the path where the previous model is stored. For (i), set `retrain` to `none`.

Using a single GPU without any of the memory optimization methods of the original ResNet (e.g. shareGradInput, optnet).
In case you want to evaluate on CPU, you should convert cudnn modules to the corresponding nn (which support CPU). To do so, use convert.lua function. 


## Examples of LRW and how to evaluate on them

In fast_evaluation you will find evaluate_examples.lua, together with some files (in torch format) from LRW and its vocabulary (500 words). Run the script and verify that (at least most of) the 5 examples are correctly classified. The .t7 files are also useful in order to check how the input of the ResNet should look like.  










 
