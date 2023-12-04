--------------------------Image Captioning Project-----------------------------------

\nWe have made a image captioning machine laerning model as
\nproject for course CS550.

\nThe working and structure is explained below , for project
\nreport (model comparisons,accuracy,findings and further
\nimprovements) check out final_report.pdf

\n---------------------------------Structure------------------------------------------

\nThe directory structure is :
\n-->drive 
                    
   \n test-->                    ...(Google Drive)
       \nimage.jpg                 ...(contains 3 smaple images)
       \nimage1.jpg
       \nimage2.jpg
   \nmodels-->                     ...(Each epoch model is saved 
	\nmodel_0.h5                   in drive to efficiently
	\n:                            use resources.)
	\n:
        \nmodel_19.h5
	
	\nmodel30_0.h5
   \nimages.zip
   \niamges_30k.zip
   \ncaptions.txt
   \ncaptions_30k.txt
   \nFlickr_8k.testImages.txt
   \nFlickr_8k.trainImages.txt
   \nFlickr_30k.testImages.txt
   \nFlickr_30k.testImages.txt

\n-->Flicker8k
     \nimagexxx.jpg
     \n:
     \n:

\n-->Flicker30k
     \nimagexxx.jpg
     \n:
     \n:
\n-->features.pkl
\n-->features_30k.pkl

\n-------------------------------------Info---------------------------------------------

\nBelow is the Essential Information about the Working of project:

\n-- Two Datasets were used Flickr8k and Flickr30k
\n-- To Make overall process fast we extract features only once
\nand dump the featulers file using pickle library
\n-- For Image processing part we used vgg16() model.
\n-- First we clean the captions ,then we split captions files
\ninto train dataset and test dataset with given ratio
\n-- We define A LSTM model
\n-- And then we train using training set once using features
\nfrom 8k set, again with 30k set

\nNote : Due to lack of computational power T4 gpu was
\ndisconnecting frequently , so we saved intermediate epochs
\nand also needed to use multiple google accounts :).
\nstill only 1 epoch with 30k was possible , I think with more
\ntraining the 30k model would have performed even better.

\n-- And at last we evalute the models by using them predict
\nthe unseen data , the test data , and in report we have mentioned
\nindivisual BELU and Rouge scores of the model

\n--------------------------------Contribution:----------------------------------------
  
\nAtharv Shendage - Image preprocessing, feature extraction and training    
\nAshmesh Dawande - Text preprocessing ,text generation and evaluation. 

\n---------------------------------  Thank You------------------------------------------
