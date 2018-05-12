# MusicAffectClassification

In this project, I use LibROSA and Spotify package to extract features from music files (.mp3 file),
and label these songs with four different affect classes: happy, sad, angry, relax.  

Then, use the features as predicting variables and the label as target variable, train and test several machine learing models with the data.

#### The process of running the codes and examine the models:  
(0) Install Spotify package by `pip3 install spotify`, install LibROSA package by `pip3 install librosa`, install mutagen with `pip3 install mutagen`, install sklearn with `pip3 install -U scikit-learn` 

(1) Feature Extraction and labeling songs(this step takes 30 minutes to 60 minutes, so the result data files have aleady been uploaded to this repository, the location and file name will be explained later in this bullet): run Feature-Extraction.ipynb to extract features using Spotify, LibROSA and output the feature files as csv file, then labeled the instances with affect types after listening to the songs listed in the dataset.   
> The dataset for Spotify extracted features are in ./spotify_trainingdata/labeled_traingingdata_no_librosa_combine_pruned.csv  
> The dataset for LibROSA extracted features are in ./librosa_trainingdata/trainingdata_librosa.csv  

> The dataset for combined features are in ./trainingdata_both/trainingdata_both_pruned.csv    

(2) To check the result of training and testing machine learing classifiers using Spotify extracted features dataset, see `Use-Spotify-Feature.ipynb`.   

(3) To check the result of training and testing machine learing classifiers using LibROSA extracted features dataset, see `Use-Librosa-Feature.ipynb`. The code in this file consider two cases: all feature vs selected featrues, and compare the performance.  

(4) To check the result of training and testing machine learing classifier using combined features dataset, see `Use-Combined-Feature.ipynb`. The code in this file consider two cases: all feature vs selected featrues, and compare the performance.  

(5) To predict an unknow set of songs, see the result in the last two cells of Use-Combined-Feature.ipynb. The data for the demo songs are in ./DemoData/demodata_both.csv, also can try with other schemas using other csv files in the DemoData folder.
