Code for generating triplets from a given dataset and training FaceNet on triplet loss to separate face embeddings.

# Versions 
1) Python     - 3.8
2) Tensorflow - 2.5.0
3) Keras      - 2.4.3 

# Data Description
GeorgiaTech Face Database - http://www.anefian.com/research/face_reco.htm - 10 subjects  

For all the images in the dataset, cropped face images were obtained and saved using the Multi-task Cascaded Convolutional Network (MTCNN) package in Keras.  

# Calculations
## For every subject:  
    Anchor   = 10  
    Positive = 10  
    Negative = 8 images per subject * 9 negative subjects  = 72  
    Total possible triplet permutations = 10 subjects * 10 Anchor * 10 Positive * 72 Negative  
'sample_data' consists of the first ten generated triplets.

# Model
'triplet_generator' was used to generate the triplets, the FaceNet model was trained on the triplet loss using the implementation available at the Keras website: https://keras.io/examples/vision/siamese_network/  
FaceNet weights can be obtain here: https://github.com/nyoki-mtl/keras-facenet

