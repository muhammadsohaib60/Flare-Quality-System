This project aims to enhance the monitoring process of operation flare stacks by implementing computer vision algorithms for the Quality Control of flare stack video inspections. computer vision algorithms will be developed to extract measure of flare and smoke and used them to classify the quality of the flare into "Good quality" or "Bad quality," or employ multiclass classification based on specific environmental conditions.


# Project 1: Flare quality system (bonus).  

Using machine learning and computer vision techniques to classify the quality of flare stack video inspections.

### Objectives
- Deepen understanding of machine learning algorithms.
- Implement machine learning into a classification system to assess flare quality.

### Flare quality system
- Enhance flare stack monitoring process using computer vision algorithms.
- Develop algorithms to classify flare quality based on image data.

### Outcomes
- Design and implement a machine learning technique.
- Demonstrate how machine learning improves flare assessment accuracy.
- Describe advantages and limitations of machine learning.

### Problem
Two approaches to designing a system
- Approach 1: Develop a convolutional neural network (ConvNet) to classify flare quality directly from images.
- Approach 2: Design a system to extract the flare and smoke areas from the image before classification.

### Approach Used
I used a pretrained model of YOLOV8 [best](./best.pt) that helped me in generating the bounding boxes of smoke. If smoke is detected in the flare then i labeled it as bad quality, if not then i label it as good quality. I ran to code that saves the data iteratively after processing 100 images and saves the labels into a csv.

### How to Run:
- Download your images dataset from [images_data](./https://drive.google.com/file/d/12O9Qk8gOXOn-5P2Jpv2Y7FiRhUJCiCXx/view?usp=sharing)
- Unzip it inside the root folder "flare-quality-classifier"
- Update the "IMAGE_PATH" variable inside the pred.ipynb file.
- Run the pred.ipynb file.

### The Resultant Data:

The data in the CSV migh look similar to this:

|Image Name | Detection|Confidence|Quality|
|----------|----------|----------|-------|
|frame23812.jpg | smoke | 0.4232463836669922 | Bad Quality
|frame14087.jpg | smoke | 0.27062007784843445 | Bad Quality
|frame2727.jpg | smoke | 0.3842276632785797 | Bad Quality
|frame22042.jpg | No detection | 0 | Good Quality
|frame11315.jpg | smoke | 0.32728880643844604 | Bad Quality
|frame42021.jpg | No detection | 0 | Good Quality
|frame19034.jpg | No detection | 0 | Good Quality
|frame7024.jpg | smoke | 0.31985166668891907 | Bad Quality

### Learning Outcomes
- I learned how to use a pretrained model to detect smoke in the images.
- I learned how to save the data into a csv file.
- I learned how to use the data to classify the quality of the flare.
