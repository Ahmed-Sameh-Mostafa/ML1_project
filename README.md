# This is project was assigned in ITI Ai|ML Track intake 2 in machine learning 1 course
---
## The project is about head pose estimation in which we try to predict the pitch, yaw and roll given an image

### This is a demo
https://drive.google.com/file/d/1-DvnejbskFw8AUOU_MVfhwuLFEnpy3nb/view?usp=sharing

---
* In this project, I used AFLW2000 Dataset.
* I used mediapipe to extrace 468 points of the face mesh of the images in the dataset and given those points and the labels in the dataset, I try to make a model with a good accuracy to predict pitch, yaw and roll.
* After extracting the 468 points for each image in the dataset, I try to centerlize the points around a point on the nose and after that to avoid the problem that arises whenver a face is near or away from the camera we divide all points by a distance between two fixed points we pick.
* After that we still get 468 points in which every point has 2 values, x and y, and that makes the number of features 2 * 468 = 936 which is a large number, So I used a pca for dimensionality reduction.
* Then in order to increase learning, I used a min-max-scaler that makes the features in range of [0,1].
* After that I tried many models and picked the best then imporved it using grid search for hyperparameter tuning.