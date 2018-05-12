# MusicAffectClassification

In this project, I use LibROSA and Spotify package to extract features from music files (which are in mp3 format),
and label these songs with four different affect classes: happy, sad, angry, relax. 
Then, use the features as predict variables and the label as target variable, train several machine learing models with
the traing data and test them on new test data in which the features are extracted with same packages.  

#### The process of running the codes and examine the models:  
(1) Feature Extraction and labeling songs(this step takes 30 minutes to 60 minutes, so the result data files have aleady been uploaded to this repository, the location and file name will be explained later in this bullet): run Feature-Extraction.ipynb to extract features using Spotify, LibROSA and output the feature files as csv file, then labeled the instances with affect types after listening to the songs listed in the dataset. The trainning dataset for Spotify extracted features are in ./spotify_trainingdata/labeled_traingingdata_no_librosa_combine_pruned.csv, the training dataset for LibROSA extracted features are in ./librosa_trainingdata/trainingdata_librosa.csv, the training dataset for combined features are in ./trainingdata_both/trainingdata_both_pruned.csv  

(2) To check the result of training and testing machine learing classifier using Spotify extracted features dataset, see Use-Spotify-Feature.ipynb.   

(3) To check the result of training and testing machine learing classifier using LibROSA extracted features dataset, see Use-Librosa-Feature.ipynb. The code in this file consider two cases: all feature vs selected featrues, and compare the performance.  

(4) To check the result of training and testing machine learing classifier using combined features dataset, see Use-Combined-Feature.ipynb. The code in this file consider two cases: all feature vs selected featrues, and compare the performance.  

(5) To predict an unknow set of songs, see the result in the last two cells of Use-Combined-Feature.ipynb. The data for the demo songs are in ./DemoData/demodata_both.csv, also can try with other schemas using other csv files in the DemoData folder.
