# General-Purpose Audio Tagging

The objective is to predict the audio classification label for the audio files found in the audio_test folder. Some sounds are distinct and instantly recognizable, like a baby’s laugh or the strum of a guitar. Other sounds aren’t clear and are difficult to pinpoint. If you close your eyes, can you tell which of the sounds below is a chainsaw versus a blender?

Well not anymore, we can train our machines to do that for us

## Why this project 

Partly, because of the vastness of sounds we experience, no reliable automatic general-purpose audio tagging systems exist. Currently, a lot of manual effort is required for tasks like annotating sound collections and providing captions for non-speech events in audiovisual content.

To tackle this problem, Freesound (an initiative by MTG-UPF that maintains a collaborative database with over 370,000 Creative Commons Licensed sounds) and Google Research’s Machine Perception Team (creators of AudioSet, a large-scale dataset of manually annotated audio events with over 500 classes) have teamed up to develop the dataset. 

We're challenged to build a general-purpose automatic audio tagging system using a dataset of audio files covering a wide range of real-world environments. Sounds in the dataset include things like musical instruments, human sounds, domestic sounds, and animals from Freesound’s library, annotated using a vocabulary of more than 40 labels from Google’s AudioSet ontology.

## Lets Get Started

   - Data Source: https://drive.google.com/drive/folders/1u0XL43B9W0a-VDzHauIj9hQdpCcXk-S0?usp=sharing
   - File descriptions
     -	train.csv - ground truth labels and other information relating to the training audio files (see Data Fields below)
     -	audio_train.zip - a folder containing the audio (.wav) training files
     -	audio_test.zip - a folder containing the audio (.wav) test files
     -	sample_submission.csv - a sample submission file in the correct format; contains the list of files found in the audio_test folder
   - Data fields
     Each row of the train.csv file contains the following information:
     - fname: the file name
     - label: the audio classification label (ground truth)
     - manually_verified: Boolean (1 or 0) flag to indicate whether or not that annotation has been manually verified

   - Structure of Data Dir shown below:
      - Data
        - **Notebook.ipynb** _Download the notebook from github and place it here_
        - train.csv
        - test_post_competition.csv
        - audio_train  
           - audio_train
                - 00044347.wav
                - 001ca53d.wav
                - 002d256b.wav	
                - 0033e230.wav	
                     ...
      
         - audio_test
            - audio_test
                 - 00063640.wav
                 - 0013a1db.wav
                 - 002bb878.wav
                 - 002d392d.wav
                      ...

## Prerequisites
  - jupyter notebook installed ( recommend Anaconda install)
  - Install following packages from python
    ```
    conda install -c conda-forge tensorflow-gpu
    conda install -c anaconda keras-gpu 
    conda install -c anaconda scipy
    conda install -c anaconda scikit-learn
    ```
      If you have installed anaconda, you'll have rest of the libraries pre-installed for you.
