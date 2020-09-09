# Hackerearth-competition-2-friendship_goals:
HI,
I am a Machine learning/Deep learning enthusiast, student at IIT-Guwahati,branch : Mtech in Signal Processing and Machine Learning.
This repository contains Machine Learning/Deep Learning (python) code for hackerearth's friendship_goals competition (Classification Challenge)!!
U may find the dataset link below and also in the notebook containing 2803 training images and 314 test images .I have achieved a total score of 67.35 and a rank of 23/5494 on the leaderboard. 
I have also attached the google colab notebook(friend_comp.ipynb) and python(friend_comp.py) file, where u can find this implementation. 

public Dataset link = https://www.kaggle.com/bing101/friendshipgoals/download

The following are the description points regarding the hyperparameters used which gave me better results and model layers description:
1. The model was based on Transfer Learning and the base_model used was ResNet50_v2.
2. Target shape of Images were made (256x256x3).
3. Out of 190 layers in base_model it as fine tuned from layer no 180. i.e layers 0 to 180 were not trainable and from 180 onwards they were trainable.
4. Output of the base_model was GlobalavgPooled2d().
5. Followed by a Dense layer with 64 'relu' activation units and a Dropout rate of 0.2.
6. Followed by a Dense layer with 32 'relu' activation units and a Dropout rate of 0.2.
7. Followed by an final output Dense layer with 3 'softmax' activation units.
8. Model is compiled with a optimizer = Adam, learning_rate = 0.0001, loss = 'categorical_crossentropy',metrics = ['accuracy'].
9. Model is trained with a steps_per_epochs = 30 and epochs = 10.
