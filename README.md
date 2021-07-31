# Day-Night-Classifier
The day/night image dataset consists of 200 RGB color images in two categories: day and night. There are equal numbers of each example: 100 day images and 100 night images.
We're trying to build a classifier that can accurately label these images as day or night, and that relies on finding distinguishing features between the two types of images.
After building this model, it is concluded that most simple problems can be solved using traditional image processing, and doesn't need Advanced Deep Learning concepts always.

*Note: All images come from the AMOS Dataset(Archive of Many Outdoor Scenes).
You can download the dataset from [here](https://drive.google.com/drive/u/2/folders/17cnu71gZMhaqn7zeefVp7eaLxhdbryP_).*

STEPS INVOLVED--
1. Importing Libraries:
   Before starting with the project code, import the libraries that will be needed for building the model.
   
2. Load the Dataset and visulaize:
   The first few lines of code will load the training day/night images and store all of them in a variable, IMAGE_LIST. This list contains the images and their associated label      ("day" or "night"). 
   
3. Preprocess the data input images:
   This function takes in a list of image-label pairs and outputs a standardized list of resized images and numerical labels.
           * Resizing every image to a standard size
           * Encode the target variables 

4. Feature Extraction:
   Let us try to create a feature that represents the brightness in an image. We'll be extracting the average brightness using HSV colorspace. Specifically, we'll use the V          channel (a measure of brightness), add up the pixel values in the V channel, then divide that sum by the area of the image to get the average Value of the image.
   
5. Build the Classifier:
   We'll turn our average brightness feature into a classifier that takes in a standardized image and returns a predicted_label for that image. This estimate_label function should    return a value: 0 or 1 (night or day, respectively).
   
6. Evaluate the classifier and Optimize:
   This is where we test your classification algorithm using our test set of data that we set aside at the beginning of the notebook! Below, we load in the test dataset,              standardize it using the standardize function you defined above, and then shuffle it; this ensures that order will not play a role in testing accuracy.   
