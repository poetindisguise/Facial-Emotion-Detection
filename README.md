# Facial-Emotion-Detection
## How to run this project
Step 1: Make a folder named "Emotion Detection" in your google drive under "My Drive".This location is very important and should not be messed with because the code internally uses this path.

Step 2: Download all the files present in this repository, unzip the zipped folders and upload it into the same "Emotion Detection folder"

Step 3: Open the Emotion Detection.ipynb file after uploading using google collaboratory and run the file.

## Aim of the project / Problem Statement :
Given an image you need to predict if the person in the image is showing the emotion of contempt or not.

## Code Design:
Step 1: Used Open Face library for Feature extraction from the 167 input images.Out of 167 images used, 155 images are used for training and 12 images are used for testing. Out of 155 images first 57 images show contempt emotion and rest 98 images does not show contempt emotion. This generates 167 csv files of 1 row and 977 features(columns). Open face is an open source toolkit used to convert image data into a csv file format (dataset) . More details can be found at following links: (https://cmusatyalab.github.io/openface/) , (https://github.com/Prodesire/face-mask).

Step 2: Using data preprocessing techniques on the generated csv files, this includes combining all the 167 csv files into 1 csv file, normalizing the dataset and labelling the dataset.

Step 3: Developed a Genetic Algorithm (Local Search Algorithm) (wrote all the function like mutation,crossover,selection,initial population from scratch) for Feature Selection and determining the best feature set.Since genetic algorithm is a evolutionary algorith we need to do hyper parameter tuning of that algorithm and see what parameter value works best for our data. Hence I have generated another csv file named GA_Analysis which shows results using vairations parameter values.

Step 4: Training using best feature set that you got using KNN algorithm

Step 5: Testing using the test dataset
