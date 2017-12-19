# Speaker_Recognition_MFCC_GMM
Authors: Michael Chen, William Xia

This program uses Mel-frequency cepstrum coefficients for feature extraction, then generates Gaussian Mixture Models for each subject.  The models predict the subject for a given test sample by comparing its extracted features to the trained models.

## Problem 
Given the speech data of several subjects, correctly identify new speech samples belonging to one of the subjects.

## Approach
-  Find a dataset of a few people saying different phases (the dataset used is available under the dataset branch)
-  Generate and use the Mel-frequency cepstrum coefficients of the sample for feature extraction
-  Generate gaussian mixture model for each subject. The models predict the subject for a given test sample by comparing its extracted features to the trained model 

## Results
-  Each speech sample is correctly classified by its respective model
-  The Gaussian models for speakers 2 and 3 are not best modeled by their respective speakers. 

## Future Work
-  Optimize the score of a speech sample with its model over the block_size-to-num_samp ratio.
-  Optimization is also possible for the number of components used in the gaussian model generation
-  This system can be generalized to a larger number of speakers. 

## Prior Work
Links to prior work/further reading:

https://github.com/ppwwyyxx/speaker-recognition
Authors: Xinyu Zhou, Yuxin Wu, and Tiezheng Li

https://github.com/orchidas/Speaker-Recognition
Authors: Orchisama Das

The approaches described in both of these works involve using the MFCC for feature extraction. Theory and techniques of clustering are discussed in both reports. The use of gaussian mixture models is talked about Zhou, Wu, and Li in their full report. Neither of them actually use the mixture models to approach the problem. However, the approach used by this project is to use the mixture models as the basis and optimize over several factors such as the size of samples, number of samples, and number of components used in the model generation. 
