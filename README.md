Image Captioning Project
This repository contains the implementation of an image captioning machine learning model developed as a project for the CS550 course.

Project Report
For a detailed analysis of the project, including model comparisons, accuracy metrics, findings, and suggestions for further improvements, please refer to final_report.pdf.

Structure
The project directory has the following structure:

.
|-- drive
|   |-- test
|   |   |-- image.jpg
|   |   |-- image1.jpg
|   |   |-- image2.jpg
|   |-- models
|   |   |-- model_0.h5
|   |   |-- ...
|   |   |-- model_19.h5
|   |   |-- model30_0.h5
|-- images.zip
|-- images_30k.zip
|-- captions.txt
|-- captions_30k.txt
|-- Flickr_8k.testImages.txt
|-- Flickr_8k.trainImages.txt
|-- Flickr_30k.testImages.txt
|-- Flickr_30k.testImages.txt
|-- Flicker8k
|   |-- imagexxx.jpg
|   |-- ...
|-- Flicker30k
|   |-- imagexxx.jpg
|   |-- ...
|-- features.pkl
|-- features_30k.pkl

nfo
Datasets Used
Flickr8k
Flickr30k
Process Overview
Feature extraction is performed only once, and the features file is dumped using the pickle library for efficiency.
VGG16 model is utilized for image processing.
Captions are cleaned, and the caption files are split into training and testing datasets according to a given ratio.
An LSTM model is defined.
Training is conducted using the training set, first with features from the 8k dataset and then with the 30k dataset.
Note: Due to limited computational power (T4 GPU disconnecting frequently), intermediate epochs were saved. Multiple Google accounts were required. Only one epoch with the 30k dataset was feasible. With more training, the 30k model could have performed better.

Models are evaluated by predicting unseen test data. Individual BLEU and Rouge scores are reported in the project's final report.
Contribution
Atharv Shendage

Image preprocessing
Feature extraction
Model training
Ashmesh Dawande

Text preprocessing
Text generation
Evaluation
Thank You
