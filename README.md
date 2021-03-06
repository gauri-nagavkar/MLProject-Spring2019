# MLProject-Spring2019
### Faces Do Lie: Do our facial expressions always accurately convey emotion? In this project, we evaluate this by providing a testbench for comparing Facial Emotion Recognition using Computer Vision and analysis of EEG Signals. We achieved an accuracy of as high as __71.87%__ in the analysis of EEG signals.

The process: As Computer Vision and Deep Learning techniques advance, we are becoming increasingly reliant on them for various use cases. In the recent future, we are going to see an increase in Social Robots that interact with us through Verbal and Non Verbal Communication (NVC) means like humans do. Facial expressions are amognst the most universal NVCs, and we argue that the current state-of-art in facial expression-based emotion classification is NOT good enough for active usage in the robots of near future. 

To test our hypothesis, we present an emperical data analysis experiment that compares brainwave signals through EEG with state-of-art facial emotion analysis techniques. To do that, we first obtained the __DEAP: A Database for Emotion Analysis Using Physiological Signals (2011)__ and wrote our own emotion classification algorithm with the techniques studied in class. For the Facial Emotion Analysis aspect, we use the Microsoft Face API on facial emotion of candidates in the dataset. Further, we compare normalized scores between EEG emotion vectors and Face API response vectors to gauge similarity between results of the two. 

#### Challenges and Project Status
##### 1. Develop an emotion classfication tool for the EEG Data
EEG data varies widely across institutions and the changing nature of its structure demands creation of emotion analysis tools that are specific to that dataset. We were faced with a challenge to create an accurate emotion classification model. We pre-processed the data and used Principal Component Analysis to reduce dimensionality. We trained multiple models and found that the SVM was most accurate. The model is in the notebook titled __EEG_Model__. The model gives us emotion scores as benchmark for comparing the facial emotion values to.

##### 2. Video Data Analysis
The facial expression data was videos of participants' faces as they react to certain experimental environmental stimuli. Since the Face API accepts only images as input, we use OpenCV to first seperate frames of the video and process every 15th frame using the API. We wrote Python code that is in the notebook __Video_Processing__ to seperate the frames and access Face API to retrieve classification scores.

##### 3. Comparitive Analysis
To answer our question, we need a statistical understanding of how the two tools perform. We used sklearn to find correlation between the vector emotion values obtained from the two techniques. 

#### EEG
Assessing and analyzing the human brain waves are of great importance in vast medical procedures. The Electroencephalogram (EEG), offers a measure of detection of abnormalities to these brain waves or, electrical signals. It is our goal to reproduce the analysis of the cortical arousal and candidates’ self-assessment scores correlations associated with psycho-physiological states, as accomplished previously by an IEEE study (S. Koelstra, et.al. DEAP: A Database for Emotion Analysis Using Physiological Signals, 2011).

#### Microsoft Face API
The Azure Cognitive Services Face API provides algorithms that are used to detect, recognize, and analyze human faces in images. It also classifies each input face into a particular emotion class with a confidence score.

### DATA
Here we describe the nature and shape of the dataset used. The DEAP dataset is access restricted and we had to apply for access for the project so we cannot share the data on Github. The dataset was generated by showing 32 candidates one minute long video clips of 40 music videos. Their physiological data and facial expressions were recorded simultaneously while the candidates watched and listened to the music videos. The candidates then evaluated the music videos based on the intensity of the emotions that they felt. Thus the DEAP dataset consists of three parts:
* 32 EEG Signals
* 1280 Video clips of facial expressions (32 candidates x 40 music videos)
* Emotion labels (for training the tool) obtained by surverying participants



### RESULTS
#### EEG Classification
We trained various classification models on the preprocessed EEG data and obtained a maximum accuracy of 71% using linear Support Vector Machine classifier. 
