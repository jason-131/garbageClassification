# Garbage Classification

This project uses AI to classify different types of garbage. 

![image](https://github.com/jason-131/garbageClassification/assets/30334711/257a00c9-84fd-4378-b5c6-28c896d3e484)


## The Algorithm

The project was made using the Jetson Nano. The Jetson Nano comes with multiple pre-trained models which makes re-training faster and more efficent. This project uses the resnet18 model that was trained on different types of garbage with six different categories. It is then run using the imagenet.py program in order to procees and image and use the model in order to classify the garbage. 
## Running this project

1.Connect to your Jetson Nano using either headed or headless mode

2.Make sure to have jetson-inference downloaded and navigate into the jetson-inference/python/training/classification directory 
 
3.Download the labels.txt and the resnet 18.onxx model 

4.Download the dataset
 
5.Set the net and data variables as shown below:
  NET=models/trash
  DATASET=data/trash

6.Run this command to process an image 
  imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/image.jpg



## Demo Video
https://youtu.be/ehF_smcbUsA


