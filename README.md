# Bag-of-Visual-Words
The bag of visual words is an image/scene recognition technique. It takes images and converts them into visual words. These visual words are then used to create a dictionary.
The dictionary is then used to learn different images. Based on this learning, images can be classified.

The Bag Of Visual Word Paradigm is fully explained in the Bovw_details folder which contains the research papers on this technique.
The general algorithm is implemented in the code as follow:

1. Function Build vocabulary: Takes each image and computes its keypoints using SIFT. Then creates a vocabulary based on these keypoints using 
  K means
2. Function get_bag_of_sifts: This function takes all the images, and then converts them into histograms. What this essentially means is that
  we take each image, compute its Sift Keypoints. They Keypoints are then compared with words in the vocabulary. This comparison is done using Euclidean Distance 
  in my implementation. The histogram of each image consists of words on the x-axis and frequency of word in an image on the y-axis. Based on the comparisons, 
  we look at the word with minimum distance to image keypoint and then increment that word's corrosponding histogram index. That means, we get a histogram representation
  of all the images.
3. Once we have the bags of sifts, we can train a nearest neighbour classifier or SVM.
4. Both of which are implemented within the code file.

DISCLAIMER: The starter code was taken from James Hayes 2019 class on CV.
