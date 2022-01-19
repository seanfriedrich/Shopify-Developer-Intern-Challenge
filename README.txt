I have created a content-based image retrieval system using Python and the OpenCV library.

The system indexes a free image dataset I found online that contains vacation photos. 

The index.py program indexes the images and creates a csv of features for each image.

The searcher.py program receives an image from the search.py program and compares its features to the features of all the indexed 
images. Using the chi-squared distance between the features in the index and the given image, the most similar images are found.

Application Instructions:

1) Open a command terminal in the location of the given python programs and the dataset

2) In the terminal, run the command: python index.py --dataset dataset --index index.csv
   This will index the dataset I have provided and create a feature set for each image that is stored in image.csv

3) Now you are ready to search. Run the command: python search.py --index index.csv --query dataset/106200.jpg --result-path dataset
   The arguments given are for the location of the index.csv file, the image that the search engine is using, and the dataset.

   In the command I gave, the image file 106200.jpg is one of many images that exist in the dataset, any other filename existing in the
   dataset can be used. I have found that 106200.jpg gives good results. Other images I tried sometimes resulted images not similar 
   to the given image being returned.

   If the image given does not exist in the dataset, an error will be thrown. 
   If the image exists in the dataset, the most similar images will be shown. 