--------------------------Image Captioning Project-----------------------------------

We have made a image captioning machine laerning model as
project for course CS550.

The working and structure is explained below , for project
report (model comparisons,accuracy,findings and further
improvements) check out final_report.pdf

---------------------------------Structure------------------------------------------

The directory structure is :
-->drive 
                    
   \n test-->                       ...(Google Drive)
       image.jpg                 ...(contains 3 smaple images)
       image1.jpg
       image2.jpg
   models-->                     ...(Each epoch model is saved 
	model_0.h5                   in drive to efficiently
	:                            use resources.)
	:
        model_19.h5
	
	model30_0.h5
   images.zip
   iamges_30k.zip
   captions.txt
   captions_30k.txt
   Flickr_8k.testImages.txt
   Flickr_8k.trainImages.txt
   Flickr_30k.testImages.txt
   Flickr_30k.testImages.txt

-->Flicker8k
     imagexxx.jpg
     :
     :

-->Flicker30k
     imagexxx.jpg
     :
     :
-->features.pkl
-->features_30k.pkl

-------------------------------------Info---------------------------------------------

Below is the Essential Information about the Working of project:

-- Two Datasets were used Flickr8k and Flickr30k
-- To Make overall process fast we extract features only once
and dump the featulers file using pickle library
-- For Image processing part we used vgg16() model.
-- First we clean the captions ,then we split captions files
into train dataset and test dataset with given ratio
-- We define A LSTM model
-- And then we train using training set once using features
from 8k set, again with 30k set

Note : Due to lack of computational power T4 gpu was
disconnecting frequently , so we saved intermediate epochs
and also needed to use multiple google accounts :).
still only 1 epoch with 30k was possible , I think with more
training the 30k model would have performed even better.

-- And at last we evalute the models by using them predict
the unseen data , the test data , and in report we have mentioned
indivisual BELU and Rouge scores of the model

--------------------------------Contribution:----------------------------------------
  
Atharv Shendage - Image preprocessing, feature extraction and training    
Ashmesh Dawande - Text preprocessing ,text generation and evaluation. 

---------------------------------  Thank You------------------------------------------
