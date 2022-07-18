# DACON_AI
* 목적: Ego-Vision 관점의 영상에서 추출한 이미지 학습데이터를 활용한 인공지능 모델 기반의 손동작 인식 및 분류 모델 개발

![Untitled (1)](https://user-images.githubusercontent.com/66737392/179512553-e2c01d71-5cac-4546-a9d7-9ea37f424163.png)
#1. Task 
   * The objective is to classify a certain hand gesture given an image. There were a total of 196 different types of hand gestures. 

#2. Data 
   * 6~7 image files of gesture. Each image file contains keypoints annotated as json file. Each keypoint is a 3 dimensional coordinate, 21 keypoints per hand. 

#3. Approach 
   * Nearest Neighbor 
      * The keypoints per image are combined into a coordinate as a 63 dimensional feature vector. We chose 'k' number of neighbors in the test dataset that had similar feature vectors to the training dataset and chose the most common label as the test label. In order to prevent the features being affected by the positioning of the hand, i.e. distance from focal point, we averaged out every key point. 
