# PyTorch-AI-road-detection
Artificial intelligence, model, training loop, model loader, inference

AI model trained on custom dataset (1000 photos). <br/>
Learning rate = 0.0001<br/>
Optimizer = Adam<br/>
Results example from video.<br/>
Results could be better but due to low memory ofGPU this is Maximum quality. 
![Road](https://github.com/Samuel-Bachorik/PyTorch-AI-road-detection/blob/main/Images/Road.gif)![Road](https://github.com/Samuel-Bachorik/PyTorch-AI-road-detection/blob/main/Images/Road2.gif)<br/>


# The course of the loss function
100-120 epoch is enough for this model with this dataset.  

![Loss](https://github.com/Samuel-Bachorik/PyTorch-AI-road-detection/blob/main/Images/Loss%20function.jpg)

# Dataset
Dataset consists of 1000 photos from rainy and sunny city. 50% rainy / 50% sunny photos<br/>
Link to dataset photos -
[Dataset](https://drive.google.com/drive/folders/1795opF54wK76r5snXs68OtGl2cR7g-3C?usp=sharing)<br/>
Example:<br/>
![Mask](https://github.com/Samuel-Bachorik/PyTorch-AI-road-detection/blob/main/Images/Image%20%26%20Mask.jpg)

# How to use 
In Run_training.py set floders with download dataset like this <br/>

```python
folders_training.append("C:/Users/Samuel/PycharmProjects/Condapytorch/mestodataset2/City_sunny1/")
folders_training.append("C:/Users/Samuel/PycharmProjects/Condapytorch/mestodataset2/City_sunny2/")
folders_training.append("C:/Users/Samuel/PycharmProjects/Condapytorch/mestodataset2/City_rainy/")
folders_training.append("C:/Users/Samuel/PycharmProjects/Condapytorch/mestodataset2/City_rainy2/")
```
Then Run Run_training.py <br/>
<br/>
When model is trained you can run inference like this -<br/>
In segmentation_inference set saved model Path <br/>
```python
# Path to trained weights
self.PATH = "./Model1"
```
In Run_video_inference.py set your desired video<br/>
```python
cap = cv2.VideoCapture("C:/Users/Samuel/PycharmProjects/Condapytorch/City.mp4")
```
Run Run_video_inference.py<br/>
When inference is done you will get output.avi video. 


# Run with pretrained model
If you want to run inference with pretrained model - (you can choose)<br/>
[Models](https://github.com/Samuel-Bachorik/PyTorch-AI-road-detection/tree/main/Modelsg)<br/>

Just In Run_video_inference.py set your desired video <br/>
```python
cap = cv2.VideoCapture("C:/Users/Samuel/PycharmProjects/Condapytorch/City.mp4")
```
In segmentation_inference set model Path <br/>
```python
# Path to trained weights
self.PATH = "./Model1"
```
In Run_video_inference.py set your desired video<br/>
```python
cap = cv2.VideoCapture("C:/Users/Samuel/PycharmProjects/Condapytorch/City.mp4")
```
Run Run_video_inference.py<br/>
When inference is done you will get output.avi video. <br/>
