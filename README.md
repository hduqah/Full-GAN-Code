README- Full GAN Code
This repository contains code for training a GAN model that generates keypoints based on input text. The model uses Tensorflow and Keras for building and training the GAN.

Overview -
The code is divided into several sections:

1. Setting the constants
2. Splitting and loading data
3. Tokenizing and preprocessing text and keypoints data
4. Creating the text encoder model
5. Building and training the GAN

Dependencies -
- Python 3.6 or above
- Tensorflow 2.x
- Numpy

Dataset Structure -
The dataset should be placed in a folder named 'Example2_filtered' with the following structure:

Example2_filtered/
    match1/
        subtitle1.txt
        keypoints1/
		1_keypoints.json
		2_keypoints.json
       		...
    match2/
        subtitle2.txt
   	keypoints1/
		1_keypoints.json
		2_keypoints.json
       		...
    ...
	
Each folder represents a match, containing a subtitle file and several keypoints files. The subtitle files should contain text in a single line. The keypoints files should be in JSON format, containing keypoints information for different body parts.
In depth instructions on how to achieve this data structure from the raw dataset are explained in the report.

Usage -
Simply run the provided code in your preferred Python environment. The code will load the dataset, preprocess the data, build and train the GAN model. After training, you can use the trained generator model to create new keypoints based on input text.

Output -
The training process will print the loss and accuracy for the discriminator (D) and generator (G) models for each epoch. You can use these values to monitor the training process and determine the quality of the generated keypoints.
