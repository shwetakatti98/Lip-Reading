# LipNet: End-to-End Sentence-level Lipreading


## Dependencies
* Keras 2.0+
* Tensorflow 1.0+
* PIP (for package installation)

Plus several other libraries listed on `setup.py`

## Usage
To use the model, first you need to clone the repository:
```
git clone https://github.com/rizkiarm/LipNet
```
Then you can install the package:
```
cd LipNet/
pip install -e .
```
**Note:** if you don't want to use CUDA, you need to edit the ``setup.py`` and change ``tensorflow-gpu`` to ``tensorflow``


## Dataset
This model uses GRID corpus (http://spandh.dcs.shef.ac.uk/gridcorpus/)

## Pre-trained weights
For those of you who are having difficulties in training the model (or just want to see the end results), you can download and use the weights provided here: https://github.com/rizkiarm/LipNet/tree/master/evaluation/models. 

More detail on saving and loading weights can be found in [Keras FAQ](https://keras.io/getting-started/faq/#how-can-i-save-a-keras-model).

## Training
There are five different training scenarios that are (going to be) available:

### Prerequisites
1. Download all video (normal) and align from the GRID Corpus website.
2. Extracts all the videos and aligns.
3. Create ``datasets`` folder on each training scenario folder.
4. Create ``align`` folder inside the ``datasets`` folder.
5. All current ``train.py`` expect the videos to be in the form of 100x50px mouthcrop image frames.
You can change this by adding ``vtype = "face"`` and ``face_predictor_path`` (which can be found in ``evaluation/models``) in the instantiation of ``Generator`` inside the ``train.py``
6. The other way would be to extract the mouthcrop image using ``scripts/extract_mouth_batch.py`` (usage can be found inside the script).
7. Create symlink from each ``training/*/datasets/align`` to your align folder.
8. You can change the training parameters by modifying ``train.py`` inside its respective scenarios.

### Random split (Unmaintained)
Create symlink from ``training/random_split/datasets/video`` to your video dataset folder (which contains ``s*`` directory).


## Evaluation
To evaluate and visualize the trained model on a single video / image frames, you can execute the following command:
```
./predict [path to weight] [path to video]
```
**Example:**
```
./predict evaluation/models/overlapped-weights368.h5 evaluation/samples/id2_vcd_swwp2s.mpg
```

## License
MIT License
