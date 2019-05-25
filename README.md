# MLProject-Spring2019
### Faces Do Lie: Do our facial expressions always accurately convey emotion? In this project, we evaluate this by providing a testbench for comparing Facial Emotion Recognition using Computer Vision and analysis of EEG Signals. 

The process: As Computer Vision and Deep Learning techniques advance, we are becoming increasingly reliant on them for various use cases. In the recent future, we are going to see an increase in Social Robots that interact with us through Verbal and Non Verbal Communication (NVC) means like humans do. Facial expressions are amognst the most universal NVCs, and we argue that the current state-of-art in facial expression-based emotion classification is NOT good enough for active usage in the robots of near future. 

To test our hypothesis, we present an emperical data analysis experiment that compares brainwave signals through EEG with state-of-art facial emotion analysis techniques. To do that, we first obtained the __DEAP: A Database for Emotion Analysis Using Physiological Signals (2011)__ and wrote our own emotion classification algorithm with the techniques studied in class. For the Facial Emotion Analysis aspect, we use the Microsoft Face API on facial emotion of candidates in the dataset. Further, we compare normalized scores between EEG emotion vectors and Face API response vectors to gauge similarity between results of the two. 

#### EEG
Assessing and analyzing the human brain waves are of great importance in vast medical procedures. The Electroencephalogram (EEG), offers a measure of detection of abnormalities to these brain waves or, electrical signals. It is our goal to reproduce the analysis of the cortical arousal and candidates’ self-assessment scores correlations associated with psycho-physiological states, as accomplished previously by an IEEE study (S. Koelstra, et.al. DEAP: A Database for Emotion Analysis Using Physiological Signals, 2011).

#### Microsoft Face API


