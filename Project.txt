## VOICE BASED VIRTUAL ASSISTANT USING NLP AND ML
Project by [Syed Luqmaan](httpswww.youtube.comchannelUCO8as7whRck3yfbaqVp2-5w)

## Contents
- [Objective](httpsgithub.comLonecarcassPortfolioeditmainREADME.md#problem-statement)
- [Summary of Project](httpsgithub.comLonecarcassPortfolioeditmainREADME.md#summary-of-project)
- [Training the Model](httpsgithub.comLonecarcassPortfolioeditmainREADME.md#training-the-model)
- [Voice Command Classifier](httpsgithub.comLonecarcassPortfolioeditmainREADME.md#voice-command-classifier)

## Objective
A modular and easily modifiable assistant can be an immensely valuable asset.
A simplified voice-based interface can allow users to get the most out of their assistant without any prior knowledge of coding.
It can be programmed to automate nearly an endless number of tasks.

## Summary of Project
I chose to write the program in python as it has a lot of libraries i require. The first problem was to record human speech and process it into text 
that the program can work with, I chose the CMU Sphinx library to do this. I used the SVM module from the library SciKitLearn to train
a model that links specific phrases to pre-defined functions. 

## Training the Model
The training data is stored in a CSV file with the first value being the name of the function and subsequent values being variants of the voice
command the user might use to call the function. The phrases are converted to word vectors, which allows for variations in voice commands as words
with similar meanings have similar vector values. The function names and word vectors are then used to fit a model (SVC with the linear kernel).

## Voice Command Classifier
The speech recognition library turns the voice commands into strings. The strings are fed into the model and the prediction is used as a 
handle to call the respective function. A separate file contains all the predefined functions. These functions could carry out any number of tasks such
as telling the time, setting a timer, reporting the weather etc.
